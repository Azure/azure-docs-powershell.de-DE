---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/new-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/New-AzureRmContainerGroup.md
ms.openlocfilehash: 30635aa9bc1906c9e329e605327df1a2dfce5df4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478558"
---
# <span data-ttu-id="969ff-101">New-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="969ff-101">New-AzureRmContainerGroup</span></span>

## <span data-ttu-id="969ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="969ff-102">SYNOPSIS</span></span>
<span data-ttu-id="969ff-103">Erstellt eine Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="969ff-103">Creates a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="969ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="969ff-104">SYNTAX</span></span>

### <span data-ttu-id="969ff-105">CreateContainerGroupBaseParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="969ff-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="969ff-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="969ff-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="969ff-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="969ff-107">DESCRIPTION</span></span>
<span data-ttu-id="969ff-108">Mit den Cmdlets **New-AzureRmContainerGroup** wird eine Containergruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="969ff-108">The **New-AzureRmContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="969ff-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="969ff-109">EXAMPLES</span></span>

### <span data-ttu-id="969ff-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="969ff-110">Example 1</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="969ff-111">Mit diesen Befehlen wird eine Containergruppe mit dem neuesten nginx-Bild erstellt und eine öffentliche IP-Adresse mit dem Öffnen von Port 8000 angefordert.</span><span class="sxs-lookup"><span data-stu-id="969ff-111">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="969ff-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="969ff-112">Example 2</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="969ff-113">Mit diesen Befehlen wird eine Containergruppe erstellt und ein benutzerdefiniertes Skript im Container ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="969ff-113">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="969ff-114">Beispiel 3: erstellt eine Containergruppe für die Fertigstellung.</span><span class="sxs-lookup"><span data-stu-id="969ff-114">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                :
Ports                    :
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="969ff-115">Mit diesen Befehlen wird eine Containergruppe erstellt, die "Hallo" ausgibt und angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="969ff-115">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="969ff-116">Beispiel 4: Erstellen einer Containergruppe mithilfe von Image in der Azure-Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="969ff-116">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myacr}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="969ff-117">Mit diesen Befehlen wird eine Containergruppe mit einem nginx-Bild in der Azure-Container Registrierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="969ff-117">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="969ff-118">Beispiel 5: Erstellen einer Containergruppe mithilfe von Bild in der benutzerdefinierten Container Bildregistrierung</span><span class="sxs-lookup"><span data-stu-id="969ff-118">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="969ff-119">Mit diesen Befehlen wird eine Containergruppe mithilfe eines benutzerdefinierten Bilds aus einer benutzerdefinierten Container Bildregistrierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="969ff-119">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="969ff-120">Beispiel 6: erstellt eine Containergruppe, die das Azure-Datei Volumen einhängt</span><span class="sxs-lookup"><span data-stu-id="969ff-120">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image alpine -AzureFileVolumeShareName myshare -AzureFileVolumeAccountKey $mycred -AzureFileVolumeMountPath /mnt/azfile

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Creating
Containers               : {mycontainer}
ImageRegistryCredentials : {myserver.com}
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {80}
OsType                   : Linux
Volumes                  : {AzureFile}
State                    : Running
Events                   : {}
```

<span data-ttu-id="969ff-121">Mit diesen Befehlen wird eine Containergruppe erstellt, in der die bereitgestellte Azure-Dateifreigabe bereitgestellt wird `/mnt/azfile` .</span><span class="sxs-lookup"><span data-stu-id="969ff-121">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

## <span data-ttu-id="969ff-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="969ff-122">PARAMETERS</span></span>

### <span data-ttu-id="969ff-123">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="969ff-123">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="969ff-124">Die Speicherkonto Anmeldeinformationen der Azure-Dateifreigabe für die Bereitstellung, wobei der Benutzername der Name des speicherkontos ist und der Schlüssel der speicherkontoschlüssel ist.</span><span class="sxs-lookup"><span data-stu-id="969ff-124">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-125">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="969ff-125">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="969ff-126">Der Bereitstellungspfad für das Azure-Datei Volume.</span><span class="sxs-lookup"><span data-stu-id="969ff-126">The mount path for the Azure File volume.</span></span>

```yaml
Type: String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-127">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="969ff-127">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="969ff-128">Der Name der Azure-Dateifreigabe, die bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="969ff-128">The name of the Azure File share to mount.</span></span>

```yaml
Type: String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-129">-Befehl</span><span class="sxs-lookup"><span data-stu-id="969ff-129">-Command</span></span>
<span data-ttu-id="969ff-130">Der Befehl, der im Container ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="969ff-130">The command to run in the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-131">-CPU</span><span class="sxs-lookup"><span data-stu-id="969ff-131">-Cpu</span></span>
<span data-ttu-id="969ff-132">Die erforderlichen CPU-Kerne.</span><span class="sxs-lookup"><span data-stu-id="969ff-132">The required CPU cores.</span></span>
<span data-ttu-id="969ff-133">Standard: 1</span><span class="sxs-lookup"><span data-stu-id="969ff-133">Default: 1</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="969ff-134">-DefaultProfile</span></span>
<span data-ttu-id="969ff-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="969ff-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-136">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="969ff-136">-DnsNameLabel</span></span>
<span data-ttu-id="969ff-137">Die DNS-Namensbezeichnung für die IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="969ff-137">The DNS name label for the IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-138">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="969ff-138">-EnvironmentVariable</span></span>
<span data-ttu-id="969ff-139">Die Container Umgebungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="969ff-139">The container environment variables.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-140">-Bild</span><span class="sxs-lookup"><span data-stu-id="969ff-140">-Image</span></span>
<span data-ttu-id="969ff-141">Das Container Bild.</span><span class="sxs-lookup"><span data-stu-id="969ff-141">The container image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-142">-Ipaddresstype</span><span class="sxs-lookup"><span data-stu-id="969ff-142">-IpAddressType</span></span>
<span data-ttu-id="969ff-143">Der Typ der IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="969ff-143">The IP address type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Public

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-144">-Standort</span><span class="sxs-lookup"><span data-stu-id="969ff-144">-Location</span></span>
<span data-ttu-id="969ff-145">Der Speicherort der Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="969ff-145">The container group Location.</span></span>
<span data-ttu-id="969ff-146">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="969ff-146">Default to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-147">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="969ff-147">-MemoryInGB</span></span>
<span data-ttu-id="969ff-148">Der erforderliche Arbeitsspeicher in GB.</span><span class="sxs-lookup"><span data-stu-id="969ff-148">The required memory in GB.</span></span>
<span data-ttu-id="969ff-149">Standard: 1,5</span><span class="sxs-lookup"><span data-stu-id="969ff-149">Default: 1.5</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: Memory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-150">-Name</span><span class="sxs-lookup"><span data-stu-id="969ff-150">-Name</span></span>
<span data-ttu-id="969ff-151">Der Name der Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="969ff-151">The container group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-152">-OsType</span><span class="sxs-lookup"><span data-stu-id="969ff-152">-OsType</span></span>
<span data-ttu-id="969ff-153">Der Typ des Container-Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="969ff-153">The container OS type.</span></span>
<span data-ttu-id="969ff-154">Standard: Linux</span><span class="sxs-lookup"><span data-stu-id="969ff-154">Default: Linux</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Linux, Windows

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-155">-Port</span><span class="sxs-lookup"><span data-stu-id="969ff-155">-Port</span></span>
<span data-ttu-id="969ff-156">Der zu öffnende Port (s).</span><span class="sxs-lookup"><span data-stu-id="969ff-156">The port(s) to open.</span></span> <span data-ttu-id="969ff-157">Standard: [80]</span><span class="sxs-lookup"><span data-stu-id="969ff-157">Default: [80]</span></span>

```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-158">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="969ff-158">-RegistryCredential</span></span>
<span data-ttu-id="969ff-159">Die Anmeldeinformationen für benutzerdefinierte Container-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="969ff-159">The custom container registry credential.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-160">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="969ff-160">-RegistryServerDomain</span></span>
<span data-ttu-id="969ff-161">Der benutzerdefinierte Container Registrierungs Anmeldeserver.</span><span class="sxs-lookup"><span data-stu-id="969ff-161">The custom container registry login server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="969ff-162">-ResourceGroupName</span></span>
<span data-ttu-id="969ff-163">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="969ff-163">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-164">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="969ff-164">-RestartPolicy</span></span>
<span data-ttu-id="969ff-165">Die Richtlinie für den Neustart des Containers.</span><span class="sxs-lookup"><span data-stu-id="969ff-165">The container restart policy.</span></span> <span data-ttu-id="969ff-166">Standard: immer</span><span class="sxs-lookup"><span data-stu-id="969ff-166">Default: Always</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Always, Never, OnFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="969ff-167">-Tag</span></span>
<span data-ttu-id="969ff-168">{{Fill Tag Description}}</span><span class="sxs-lookup"><span data-stu-id="969ff-168">{{Fill Tag Description}}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-169">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="969ff-169">-Confirm</span></span>
<span data-ttu-id="969ff-170">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="969ff-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="969ff-171">-WhatIf</span></span>
<span data-ttu-id="969ff-172">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="969ff-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="969ff-173">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="969ff-173">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969ff-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="969ff-174">CommonParameters</span></span>
<span data-ttu-id="969ff-175">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="969ff-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="969ff-176">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="969ff-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="969ff-177">Eingaben</span><span class="sxs-lookup"><span data-stu-id="969ff-177">INPUTS</span></span>

### <span data-ttu-id="969ff-178">System. String</span><span class="sxs-lookup"><span data-stu-id="969ff-178">System.String</span></span>
<span data-ttu-id="969ff-179">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="969ff-179">System.Collections.Hashtable</span></span>

## <span data-ttu-id="969ff-180">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="969ff-180">OUTPUTS</span></span>

### <span data-ttu-id="969ff-181">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="969ff-181">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="969ff-182">Notizen</span><span class="sxs-lookup"><span data-stu-id="969ff-182">NOTES</span></span>

## <span data-ttu-id="969ff-183">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="969ff-183">RELATED LINKS</span></span>
