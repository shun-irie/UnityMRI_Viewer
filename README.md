# UnityMRI_Viewer
## 1. 利用目的
MRI画像をUnityに組み込みたいという方のためのツール
## 2. MRI画像のソース
標準脳データ（MNI152.nii.gz）を用いて、1mmごとに自動生成させました。
## 3. Copy Right
作成者: 入江　駿（獨協医科大学　講師）
複製・改変ともにクレジット表記の必要はありません。
## 4. 使い方
### (1) MRI_Viewer_for_Unity.unitypackageのインポート
### (2) パッケージ内のツールを開く
### (3) Playボタンを押す. 以上
## 5. 仕組み
### MRI_controller.cs
MRI画像をRawImageのTextureとして更新します。ご使用の環境に合わせてbase_path（MRI画像のフォルダ）を変更してください
public int x, y, zはそれぞれMNI座標を意味し、それぞれの値を更新することで、MNIに一致する断面を抽出します
### LineControler.cs
各断面におけるx,y,zの位置を線で表しています。線はRawImageで作っています。
これは他のアプリとの連携方法についての説明のために作っています。
'''cs
public class LineControler : MonoBehaviour
{
    MRI_controller mri;//これによりMRI_controllerでのpublic変数にアクセス可能になります
'''
