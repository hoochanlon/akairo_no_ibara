# ȷ���ű��׳������Ĵ���
set -e

cd _site

if [ -d ".git" ];then
  rm -rf  .git
fi
# ����Ƿ������Զ�������
# echo 'www.example.com' > CNAME
# �ű��ο� http://wmm66.com/index/article/detail/id/62.html

git init
git add .
sudo git commit -m 'deploy'
git remote add origin https://github.com/hoochanlon/hoochanlon.github.io.git
git checkout -b gh-pages
sudo git push origin gh-pages -f

cd -

##git

git remote set-url origin repo.git //�޸�Զ�ֿ̲��ַ
git push origin :branch-name //ɾ��Զ�̷�֧
git reset --hard origin/master  //ָ���HEADָ��master���°汾
git pull //ǿ�кϲ�
