
// Image output and input
#include 
#include

int main() {
using namespace std;
const int w = 750;
const int h = 500;

const char* IFile = "unesco750-1.raw";
const char* OFile1 = "reverse_intensity.raw";
const char* OFile2 = "add_20pixel.raw";
const char* OFile3 = "add_100pixel.raw";


FILE* InFile = fopen(IFile, "rb");
if (!InFile) {
    cout<<"Failed to open input file";
    return 1;}



FILE* OutFile1 = fopen(OFile1, "wb");
FILE* OutFile2 = fopen(OFile2, "wb");
FILE* OutFile3 = fopen(OFile3, "wb");


if (!OutFile1 || !OutFile2 || !OutFile3) {
    cout<<"Failed to open output file(s)";
    fclose(InFile);
    fclose(OutFile1);
    fclose(OutFile2);
    fclose(OutFile3);
    return 1;}


unsigned char img1[h][w];
unsigned char img2[h][w];
unsigned char img3[h][w];


fread(img1, sizeof(unsigned char), w * h, InFile);
 fseek(InFile, 0, SEEK_SET);
fread(img2, sizeof(unsigned char), w * h, InFile);
 fseek(InFile, 0, SEEK_SET);
fread(img3, sizeof(unsigned char), w * h, InFile);
 fseek(InFile, 0, SEEK_SET);


for (int j = 0; j < h; j++) {
    for (int i = 0; i < w; i++) {
       
        img1[j][i] = 255 - img1[j][i];
        
      
        img2[j][i] = 20 + img2[j][i];
        
        
        img3[j][i] = 100 + img3[j][i];}}
    


fwrite(img1, sizeof(unsigned char), w * h, OutFile1);
fwrite(img2, sizeof(unsigned char), w * h, OutFile2);
fwrite(img3, sizeof(unsigned char), w * h, OutFile3);

fclose(InFile);
fclose(OutFile1);
fclose(OutFile2);
fclose(OutFile3);

return 0;
}
