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

