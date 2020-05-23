ARG SERVERCORE_VERSION=1909
FROM mcr.microsoft.com/windows/servercore:${SERVERCORE_VERSION}

# Download latest miniconda installer
RUN powershell.exe -Command Invoke-WebRequest -Uri https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe -OutFile C:\miniconda3.exe

# Execute installation
RUN powershell.exe -Command Start-Process C:\miniconda3.exe -ArgumentList '/S', '/D=C:\miniconda3' -Wait

# Remove installation file
RUN powershell.exe -Command rm C:\miniconda3.exe

# Initialize powershell for usage with conda
RUN C:\miniconda3\Scripts\conda.exe init powershell

# Update conda
RUN powershell.exe -Command conda update conda --yes --quiet

# Clean conda
RUN powershell.exe -Command conda clean --all --quiet --yes

CMD [ "powershell.exe" ]
