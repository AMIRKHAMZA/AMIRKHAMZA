- 👋 Hi, I’m @AMIRKHAMZA
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
AMIRKHAMZA/AMIRKHAMZA is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
        run: ./ci/run_tests.sh "${{ matrix.test-env }}" "${{ matrix.container }}"
      - name: Upload pytest-mpl artifacts
        if: failure()
        uses: actions/upload-artifact@v3
        uses: actions/upload-artifact@v4
        with:
          name: pytest-mpl-results
          path: /tmp/oggm-mpl-results/
          
