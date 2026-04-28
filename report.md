mkdir -p ~/projects
cd ~/projects
git clone https://github.com/tp-labs/lab03.git
cd lab03
git remote remove origin
git remote add origin git@github.com:USERNAME/lab03.git

cmake -S . -B build
cmake --build build

./build/hello_world_application/hello_world
echo "1 5 4" | ./build/solver_application/solver_application

git add .
git commit -m "Add CMake build files for lab03"
git branch -M main
git push -u origin main
