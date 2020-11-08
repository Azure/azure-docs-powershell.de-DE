---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/new-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/New-AzContainerGroup.md
ms.openlocfilehash: 20daa8d14f77ca4563c072d58d1c2269235cb164
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176953"
---
# <span data-ttu-id="4b301-101">New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="4b301-101">New-AzContainerGroup</span></span>

## <span data-ttu-id="4b301-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b301-102">SYNOPSIS</span></span>
<span data-ttu-id="4b301-103">Erstellt eine Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="4b301-103">Creates a container group.</span></span>

## <span data-ttu-id="4b301-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b301-104">SYNTAX</span></span>

### <span data-ttu-id="4b301-105">CreateContainerGroupBaseParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4b301-105">CreateContainerGroupBaseParamSet (Default)</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] [-AssignIdentity] [-OsType <String>]
 [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>]
 [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>] [-EnvironmentVariable <Hashtable>]
 [-RegistryServerDomain <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b301-106">CreateContainerGroupWithAzureFileMountParamSet</span><span class="sxs-lookup"><span data-stu-id="4b301-106">CreateContainerGroupWithAzureFileMountParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 [-AssignIdentity] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b301-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span><span class="sxs-lookup"><span data-stu-id="4b301-107">CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] -AzureFileVolumeShareName <String>
 -AzureFileVolumeAccountCredential <PSCredential> -AzureFileVolumeMountPath <String> [-Location <String>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>]
 [-Cpu <Int32>] [-MemoryInGB <Double>] [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>]
 [-Command <String>] [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b301-108">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b301-108">ExplicitIdentityParameterSet</span></span>
```
New-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-Image] <String>
 [-RegistryCredential <PSCredential>] [-Location <String>] -IdentityType <ResourceIdentityType>
 [-IdentityId <String[]>] [-OsType <String>] [-RestartPolicy <String>] [-Cpu <Int32>] [-MemoryInGB <Double>]
 [-IpAddressType <String>] [-DnsNameLabel <String>] [-Port <Int32[]>] [-Command <String>]
 [-EnvironmentVariable <Hashtable>] [-RegistryServerDomain <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b301-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b301-109">DESCRIPTION</span></span>
<span data-ttu-id="4b301-110">Mit den Cmdlets **New-AzContainerGroup** wird eine Containergruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="4b301-110">The **New-AzContainerGroup** cmdlets creates a container group.</span></span>

## <span data-ttu-id="4b301-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b301-111">EXAMPLES</span></span>

### <span data-ttu-id="4b301-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4b301-112">Example 1</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000)

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

<span data-ttu-id="4b301-113">Mit diesen Befehlen wird eine Containergruppe mit dem neuesten nginx-Bild erstellt und eine öffentliche IP-Adresse mit dem Öffnen von Port 8000 angefordert.</span><span class="sxs-lookup"><span data-stu-id="4b301-113">This commands creates a container group using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="4b301-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4b301-114">Example 2</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "/bin/sh -c myscript.sh" -EnvironmentVariable @{"env1"="value1";"env2"="value2"}

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

<span data-ttu-id="4b301-115">Mit diesen Befehlen wird eine Containergruppe erstellt und ein benutzerdefiniertes Skript im Container ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b301-115">This commands creates a container group and runs a custom script inside the container.</span></span>

### <span data-ttu-id="4b301-116">Beispiel 3: erstellt eine Containergruppe für die Fertigstellung.</span><span class="sxs-lookup"><span data-stu-id="4b301-116">Example 3: Creates a run-to-completion container group.</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image alpine -OsType Linux -Command "echo hello" -RestartPolicy Never

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

<span data-ttu-id="4b301-117">Mit diesen Befehlen wird eine Containergruppe erstellt, die "Hallo" ausgibt und angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="4b301-117">This commands creates a container group which prints out 'hello' and stops.</span></span>

### <span data-ttu-id="4b301-118">Beispiel 4: Erstellen einer Containergruppe mithilfe von Image in der Azure-Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="4b301-118">Example 4: Creates a container group using image in Azure Container Registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("myacr", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image myacr.azurecr.io/nginx:latest -IpAddressType Public -RegistryCredential $mycred

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

<span data-ttu-id="4b301-119">Mit diesen Befehlen wird eine Containergruppe mit einem nginx-Bild in der Azure-Container Registrierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="4b301-119">This commands creates a container group using a nginx image in Azure Container Registry.</span></span>

### <span data-ttu-id="4b301-120">Beispiel 5: Erstellen einer Containergruppe mithilfe von Bild in der benutzerdefinierten Container Bildregistrierung</span><span class="sxs-lookup"><span data-stu-id="4b301-120">Example 5: Creates a container group using image in custom container image registry</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer -Image myserver.com/myimage:latest -RegistryServer myserver.com -RegistryCredential $mycred

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

<span data-ttu-id="4b301-121">Mit diesen Befehlen wird eine Containergruppe mithilfe eines benutzerdefinierten Bilds aus einer benutzerdefinierten Container Bildregistrierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="4b301-121">This commands creates a container group using a custom image from a custom container image registry.</span></span>

### <span data-ttu-id="4b301-122">Beispiel 6: erstellt eine Containergruppe, die das Azure-Datei Volumen einhängt</span><span class="sxs-lookup"><span data-stu-id="4b301-122">Example 6: Creates a container group that mounts Azure File volume</span></span>
```
PS C:\> $secpasswd = ConvertTo-SecureString "PlainTextPassword" -AsPlainText -Force
PS C:\> $mycred = New-Object System.Management.Automation.PSCredential ("username", $secpasswd)
PS C:\> New-AzContainerGroup -ResourceGroupName MyResourceGroup -Name mycontainer -Image alpine -AzureFileVolumeShareName myshare -AzureFileVolumeAccountCredential $mycred -AzureFileVolumeMountPath /mnt/azfile

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

<span data-ttu-id="4b301-123">Mit diesen Befehlen wird eine Containergruppe erstellt, in der die bereitgestellte Azure-Dateifreigabe bereitgestellt wird `/mnt/azfile` .</span><span class="sxs-lookup"><span data-stu-id="4b301-123">This commands creates a container group that mounts the provided Azure File share to `/mnt/azfile`.</span></span>

### <span data-ttu-id="4b301-124">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="4b301-124">Example 7</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -AssignIdentity

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
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="4b301-125">Mit diesen Befehlen wird eine Containergruppe mit dem System zugewiesene Identität mit dem neuesten nginx-Bild erstellt, und es wird eine öffentliche IP-Adresse mit dem Öffnen von Port 8000 angefordert.</span><span class="sxs-lookup"><span data-stu-id="4b301-125">This commands creates a container group with system assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

### <span data-ttu-id="4b301-126">Beispiel 8</span><span class="sxs-lookup"><span data-stu-id="4b301-126">Example 8</span></span>
```
PS C:\> New-AzContainerGroup -ResourceGroupName demo -Name mycontainer -Image nginx -OsType Linux -IpAddressType Public -Port @(8000) -IdentityType SystemAssignedUserAssigned -IdentityId /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.ManagedIdentity/userAssignedIdentities/<UserIdentityName>

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
Identity                 : Microsoft.Azure.Management.ContainerInstance.Models.ContainerGroupIdentity
```

<span data-ttu-id="4b301-127">Mit diesen Befehlen wird eine Containergruppe mit dem System zugewiesen und der Benutzer zugewiesene Identität mithilfe des neuesten nginx-Bilds erstellt, und es wird eine öffentliche IP-Adresse mit dem Öffnen von Port 8000 angefordert.</span><span class="sxs-lookup"><span data-stu-id="4b301-127">This commands creates a container group with system assigned and user assigned identity using latest nginx image and requests a public IP address with opening port 8000.</span></span>

## <span data-ttu-id="4b301-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b301-128">PARAMETERS</span></span>

### <span data-ttu-id="4b301-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="4b301-129">-AssignIdentity</span></span>
<span data-ttu-id="4b301-130">System zugewiesene Identität aktivieren</span><span class="sxs-lookup"><span data-stu-id="4b301-130">Enable system assigned identity</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateContainerGroupBaseParamSet, CreateContainerGroupWithAzureFileMountParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-131">-AzureFileVolumeAccountCredential</span><span class="sxs-lookup"><span data-stu-id="4b301-131">-AzureFileVolumeAccountCredential</span></span>
<span data-ttu-id="4b301-132">Die Speicherkonto Anmeldeinformationen der Azure-Dateifreigabe für die Bereitstellung, wobei der Benutzername der Name des speicherkontos ist und der Schlüssel der speicherkontoschlüssel ist.</span><span class="sxs-lookup"><span data-stu-id="4b301-132">The storage account credential of the Azure File share to mount where the username is the storage account name and the key is the storage account key.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-133">-AzureFileVolumeMountPath</span><span class="sxs-lookup"><span data-stu-id="4b301-133">-AzureFileVolumeMountPath</span></span>
<span data-ttu-id="4b301-134">Der Bereitstellungspfad für das Azure-Datei Volume.</span><span class="sxs-lookup"><span data-stu-id="4b301-134">The mount path for the Azure File volume.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-135">-AzureFileVolumeShareName</span><span class="sxs-lookup"><span data-stu-id="4b301-135">-AzureFileVolumeShareName</span></span>
<span data-ttu-id="4b301-136">Der Name der Azure-Dateifreigabe, die bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b301-136">The name of the Azure File share to mount.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateContainerGroupWithAzureFileMountParamSet, CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-137">-Befehl</span><span class="sxs-lookup"><span data-stu-id="4b301-137">-Command</span></span>
<span data-ttu-id="4b301-138">Der Befehl, der im Container ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b301-138">The command to run in the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-139">-CPU</span><span class="sxs-lookup"><span data-stu-id="4b301-139">-Cpu</span></span>
<span data-ttu-id="4b301-140">Die erforderlichen CPU-Kerne.</span><span class="sxs-lookup"><span data-stu-id="4b301-140">The required CPU cores.</span></span>
<span data-ttu-id="4b301-141">Standard: 1</span><span class="sxs-lookup"><span data-stu-id="4b301-141">Default: 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b301-142">-DefaultProfile</span></span>
<span data-ttu-id="4b301-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4b301-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-144">-DnsNameLabel</span><span class="sxs-lookup"><span data-stu-id="4b301-144">-DnsNameLabel</span></span>
<span data-ttu-id="4b301-145">Die DNS-Namensbezeichnung für die IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="4b301-145">The DNS name label for the IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-146">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="4b301-146">-EnvironmentVariable</span></span>
<span data-ttu-id="4b301-147">Die Container Umgebungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="4b301-147">The container environment variables.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-148">-Identitäts Kennung</span><span class="sxs-lookup"><span data-stu-id="4b301-148">-IdentityId</span></span>
<span data-ttu-id="4b301-149">Der Benutzer hat Identitäts-IDs zugewiesen</span><span class="sxs-lookup"><span data-stu-id="4b301-149">The user assigned identity IDs</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-150">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="4b301-150">-IdentityType</span></span>
<span data-ttu-id="4b301-151">Der Typ der verwalteten Identität</span><span class="sxs-lookup"><span data-stu-id="4b301-151">The managed identity type</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerInstance.Models.ResourceIdentityType
Parameter Sets: CreateContainerGroupWithAzureFileMountAndExplicitIdentityParamSet, ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-152">-Bild</span><span class="sxs-lookup"><span data-stu-id="4b301-152">-Image</span></span>
<span data-ttu-id="4b301-153">Das Container Bild.</span><span class="sxs-lookup"><span data-stu-id="4b301-153">The container image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-154">-Ipaddresstype</span><span class="sxs-lookup"><span data-stu-id="4b301-154">-IpAddressType</span></span>
<span data-ttu-id="4b301-155">Der Typ der IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="4b301-155">The IP address type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Public

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-156">-Standort</span><span class="sxs-lookup"><span data-stu-id="4b301-156">-Location</span></span>
<span data-ttu-id="4b301-157">Der Speicherort der Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="4b301-157">The container group Location.</span></span>
<span data-ttu-id="4b301-158">Standardmäßig wird der Speicherort der Ressourcengruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b301-158">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-159">-MemoryInGB</span><span class="sxs-lookup"><span data-stu-id="4b301-159">-MemoryInGB</span></span>
<span data-ttu-id="4b301-160">Der erforderliche Arbeitsspeicher in GB.</span><span class="sxs-lookup"><span data-stu-id="4b301-160">The required memory in GB.</span></span>
<span data-ttu-id="4b301-161">Standard: 1,5</span><span class="sxs-lookup"><span data-stu-id="4b301-161">Default: 1.5</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases: Memory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-162">-Name</span><span class="sxs-lookup"><span data-stu-id="4b301-162">-Name</span></span>
<span data-ttu-id="4b301-163">Der Name der Containergruppe.</span><span class="sxs-lookup"><span data-stu-id="4b301-163">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-164">-OsType</span><span class="sxs-lookup"><span data-stu-id="4b301-164">-OsType</span></span>
<span data-ttu-id="4b301-165">Der Typ des Container-Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="4b301-165">The container OS type.</span></span>
<span data-ttu-id="4b301-166">Standard: Linux</span><span class="sxs-lookup"><span data-stu-id="4b301-166">Default: Linux</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Linux, Windows

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-167">-Port</span><span class="sxs-lookup"><span data-stu-id="4b301-167">-Port</span></span>
<span data-ttu-id="4b301-168">Der zu öffnende Port (s).</span><span class="sxs-lookup"><span data-stu-id="4b301-168">The port(s) to open.</span></span> <span data-ttu-id="4b301-169">Standard: [80]</span><span class="sxs-lookup"><span data-stu-id="4b301-169">Default: [80]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-170">-RegistryCredential</span><span class="sxs-lookup"><span data-stu-id="4b301-170">-RegistryCredential</span></span>
<span data-ttu-id="4b301-171">Die Anmeldeinformationen für benutzerdefinierte Container-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="4b301-171">The custom container registry credential.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-172">-RegistryServerDomain</span><span class="sxs-lookup"><span data-stu-id="4b301-172">-RegistryServerDomain</span></span>
<span data-ttu-id="4b301-173">Der benutzerdefinierte Container Registrierungs Anmeldeserver.</span><span class="sxs-lookup"><span data-stu-id="4b301-173">The custom container registry login server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RegistryServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b301-174">-ResourceGroupName</span></span>
<span data-ttu-id="4b301-175">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4b301-175">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-176">-RestartPolicy</span><span class="sxs-lookup"><span data-stu-id="4b301-176">-RestartPolicy</span></span>
<span data-ttu-id="4b301-177">Die Richtlinie für den Neustart des Containers.</span><span class="sxs-lookup"><span data-stu-id="4b301-177">The container restart policy.</span></span> <span data-ttu-id="4b301-178">Standard: immer</span><span class="sxs-lookup"><span data-stu-id="4b301-178">Default: Always</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Always, Never, OnFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="4b301-179">-Tag</span></span>
<span data-ttu-id="4b301-180">{{Fill Tag Description}}</span><span class="sxs-lookup"><span data-stu-id="4b301-180">{{Fill Tag Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-181">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4b301-181">-Confirm</span></span>
<span data-ttu-id="4b301-182">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b301-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b301-183">-WhatIf</span></span>
<span data-ttu-id="4b301-184">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b301-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b301-185">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b301-185">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b301-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b301-186">CommonParameters</span></span>
<span data-ttu-id="4b301-187">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b301-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b301-188">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b301-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b301-189">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b301-189">INPUTS</span></span>

### <span data-ttu-id="4b301-190">System. String</span><span class="sxs-lookup"><span data-stu-id="4b301-190">System.String</span></span>

### <span data-ttu-id="4b301-191">System. String []</span><span class="sxs-lookup"><span data-stu-id="4b301-191">System.String[]</span></span>

### <span data-ttu-id="4b301-192">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4b301-192">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4b301-193">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b301-193">OUTPUTS</span></span>

### <span data-ttu-id="4b301-194">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="4b301-194">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="4b301-195">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b301-195">NOTES</span></span>

## <span data-ttu-id="4b301-196">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b301-196">RELATED LINKS</span></span>
