#bài1

def tinh_tien_taxi(x):
    if x <= 1:
        gia_tien = 15000
    elif 1 < x <= 5:
        gia_tien = 15000 + (x - 1) * 13500
    else:
        gia_tien = 15000 + 4 * 13500 + (x - 5) * 11000

    if x > 120:
        gia_tien = (15000 + 4 * 13500 + (x - 5) * 11000)*0.9

    return gia_tien
def main():
    try:
        x=float(input("số km di được:"))
        if x<0:
            print("số km phải lớn hơn 0")
        else:
            tien_taxi=tinh_tien_taxi(x)
            print(f"số tiền taxi phải trả là:{tien_taxi}")
    except ValueError:
        print("Vui lòng nhập một số hợp lệ.")
                    
if __name__ == "__main__":
    main()

#bài2
import cmath  

def giai_phuong_trinh_bac_2(a,b,c):
    if a == 0:
        raise ValueError()
    delta = b**2 - 4*a*c

    if delta >= 0:
        x1 = (-b + (delta)**0.5) / (2*a)
        x2 = (-b - (delta)**0.5) / (2*a)
        return x1,x2
    else:
        x1 = (-b + cmath.sqrt(delta)) / (2*a)
        x2 = (-b - cmath.sqrt(delta)) / (2*a)
        return x1, x2

def main():
    try:
        a = float(input("Nhập a: "))
        b = float(input("Nhập b: "))
        c = float(input("Nhập c: "))
        
        ket_qua = giai_phuong_trinh_bac_2(a,b,c)
        print(f"Nghiệm của phương trình là: {ket_qua}")
    except ValueError:
        print("Vui lòng nhập số hợp lệ.")
if __name__ == "__main__":
    main()

#bài 3
def lay_ten_thang(t):
    thang = ["","January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"]
    if 1 <= t <= 12:
        return thang[t]
    else:
        return "Tháng không hợp lệ"

def main():
    try:
        t = int(input("Nhập số tháng (từ 1 đến 12): "))
        ten_thang = lay_ten_thang(t)
        print(f"Tháng {t} là tháng {ten_thang}")
    except ValueError:
        print(f"Vui lòng nhập một số nguyên từ 1 đến 12")

if __name__ == "__main__":
    main()

#Bài 4
def ktra_nam_nhuan(n):
    if (n % 4 == 0 and n % 100 != 0) or (n % 400 == 0):
        return True
    else:
        return False
def main():
    try:
        n = int(input("nhập năm:"))
        if ktra_nam_nhuan(n):
            print(f"{n} là năm nhuận")
        else:
            print(f"{n} không phải là năm nhuận")
    except ValueError:
        print("Hãy nhập số nguyên")
if __name__=="__main__":
    main()

#Bài 5
def xep_loai_hoc_sinh(diem_trung_binh):
    
    if diem_trung_binh >= 9.0:
        return "Xuất sắc"
    elif 8.0 <= diem_trung_binh < 9.0:
        return "Giỏi"
    elif 6.5 <= diem_trung_binh < 8.0:
        return "Khá"
    elif 5.0 <= diem_trung_binh < 6.5:
        return "Trung bình"
    elif 3.5 <= diem_trung_binh < 5.0:
        return "Yếu"
    elif 0 <= diem_trung_binh < 3.5:
        return "Kém"
    else:
        return "Điểm không hợp lệ"
def main():
    try:
        diem_trung_binh = float(input("Nhập điểm trung bình: "))
        if 0 <= diem_trung_binh <= 10:
            xep_loai = xep_loai_hoc_sinh(diem_trung_binh)
            print(f"Xếp loại học sinh: {xep_loai}")
        else:
            print("Điểm trung bình không hợp lệ. Vui lòng nhập trong khoảng từ 0 đến 10.")
    except ValueError:
        print("Vui lòng nhập một số hợp lệ.")

if __name__ == "__main__":
    main()













    


















    



