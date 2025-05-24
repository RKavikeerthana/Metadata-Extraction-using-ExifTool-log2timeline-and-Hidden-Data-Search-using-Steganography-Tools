# Metadata-Extraction-using-ExifTool-log2timeline-and-Hidden-Data-Search-using-Steganography-Tools
# Name: Kavi Keerthana R 
# Reg No: 212222100022
## AIM:
To extract metadata, perform timeline analysis, and search for hidden data using forensic tools like ExifTool, log2timeline, and steganography detection tools.

## DESIGN STEPS:
### Step 1:
Use exiftool to extract metadata from files such as images, documents, and videos.

### Step 2:
Use log2timeline and plaso to create and analyze event timelines from system logs and file metadata.

### Step 3:
Apply steganography detection tools like steghide, zsteg, or binwalk to uncover hidden data in media files.

## PROGRAM:
Metadata and Timeline Forensics, Steganography Analysis Steps
- **Installation :**
```bash
   sudo apt update
   sudo apt install exiftool -y
   sudo apt install plaso -y
   sudo apt install steghide -y
   sudo apt install binwalk -y
 ```
- **Extract metadata from a file:**
```bash
  exiftool image path
  exiftool png.jpeg
```
- **Embed data**
  ```
  steghide embed -cf (image path) -ef (text file path)
  steghide embed -cf /home/user/Desktop/test.jpeg -ef /home/user/Desktop/abc.txt
  ```
- **Extract hidden data:**
  ```
  steghide extract -sf (imamge path)
  steghide extract -sf /home/user/Desktop/test.jpeg -p 12 -xf /home/user/Downloads/abc.txt

  ```
- **Using binwalk – for file analysis**  
  ```bash
   binwalk png.jpeg
  ```
  
## OUTPUT:

### Extraction of Metadata using exiftool
![image](https://github.com/user-attachments/assets/f1403f3f-3395-4f73-9224-f52302b18c63)


### Data Embedding in Image
![image](https://github.com/user-attachments/assets/a06c1001-f102-4558-9c08-27f532b4c41f)


### Extraction of hidden data
![image](https://github.com/user-attachments/assets/fc9d34fd-9575-4648-aeab-d32322b8a8af)


### Using binwalk – for file analysis
![image](https://github.com/user-attachments/assets/c3439198-0c2c-49a8-84ac-45db97a28451)



## RESULT:
Metadata was successfully extracted, timeline analysis was completed, and hidden data was identified using steganography tools.

