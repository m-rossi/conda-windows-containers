ARG SERVERCORE_VERSION=1909
ARG MINIFORGE_VERSION=4.9.2-7
FROM mcr.microsoft.com/windows/servercore:${SERVERCORE_VERSION}-

# Download latest miniconda installer
RUN powershell.exe -Command Invoke-WebRequest -Uri https://github.com/conda-forge/miniforge/releases/download/{MINIFORGE_VERSION}/Miniforge3-{MINIFORGE_VERSION}-Windows-x86_64.exe -OutFile C:\miniforge3.exe

# Execute installation
RUN powershell.exe -Command Start-Process C:\miniforge3.exe -ArgumentList '/S', '/D=C:\miniforge3' -Wait

# Remove installation file
RUN powershell.exe -Command rm C:\miniforge3.exe

# Initialize powershell for usage with conda
RUN C:\miniforge3\Scripts\conda.exe init powershell

# Update conda
RUN powershell.exe -Command conda update conda --yes --quiet

# Clean conda
RUN powershell.exe -Command conda clean --all --quiet --yes

CMD [ "powershell.exe" ]
