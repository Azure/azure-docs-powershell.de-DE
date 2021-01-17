---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
ms.openlocfilehash: 12ab6c1948f0864c7dcb930d0a658088fd83262c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458244"
---
# <span data-ttu-id="29611-101">New-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="29611-101">New-AzStackEdgeShare</span></span>

## <span data-ttu-id="29611-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29611-102">SYNOPSIS</span></span>
<span data-ttu-id="29611-103">Erstellt eine neue Freigabe auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="29611-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="29611-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29611-104">SYNTAX</span></span>

### <span data-ttu-id="29611-105">SmbParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="29611-105">SmbParameterSet (Default)</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29611-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="29611-106">CloudShareNfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29611-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="29611-107">CloudShareSmbParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29611-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="29611-108">NfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29611-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29611-109">DESCRIPTION</span></span>
<span data-ttu-id="29611-110">Das **Cmdlet "New-AzStackEdgeShare"** erstellt eine neue Freigabe auf dem Stack Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="29611-110">The **New-AzStackEdgeShare** cmdlet creates a new share on the Stack Edge device.</span></span>

## <span data-ttu-id="29611-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="29611-111">EXAMPLES</span></span>

### <span data-ttu-id="29611-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="29611-112">Example 1</span></span>
```
PS C:\> New-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="29611-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29611-113">PARAMETERS</span></span>

### <span data-ttu-id="29611-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29611-114">-AsJob</span></span>
<span data-ttu-id="29611-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="29611-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29611-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="29611-116">-ClientAccessRight</span></span>
<span data-ttu-id="29611-117">Lese-/Schreibzugriff für clientIds, Für ex:@(@{"ClientId"="192.168.10.10";" AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";" AccessRight"="ReadOnly"})</span><span class="sxs-lookup"><span data-stu-id="29611-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29611-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="29611-118">-CloudShare</span></span>
<span data-ttu-id="29611-119">Bereitstellen des Ressourcennamens von StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="29611-119">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29611-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="29611-120">-ContainerName</span></span>
<span data-ttu-id="29611-121">Containername (basierend auf dem angegebenen Datenformat stellt dies den Namen von Azure-Dateien/-Seitenblob/-Block-BLOB dar)</span><span class="sxs-lookup"><span data-stu-id="29611-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29611-122">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="29611-122">-DataFormat</span></span>
<span data-ttu-id="29611-123">Set Data Format ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="29611-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29611-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29611-124">-DefaultProfile</span></span>
<span data-ttu-id="29611-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29611-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29611-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="29611-126">-DeviceName</span></span>
<span data-ttu-id="29611-127">Gerätename</span><span class="sxs-lookup"><span data-stu-id="29611-127">Device Name</span></span>

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

### <span data-ttu-id="29611-128">-Name</span><span class="sxs-lookup"><span data-stu-id="29611-128">-Name</span></span>
<span data-ttu-id="29611-129">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="29611-129">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29611-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="29611-130">-NFS</span></span>
<span data-ttu-id="29611-131">AccessProtocol beim Erstellen der Freigabe</span><span class="sxs-lookup"><span data-stu-id="29611-131">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29611-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29611-132">-ResourceGroupName</span></span>
<span data-ttu-id="29611-133">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="29611-133">Resource Group Name</span></span>

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

### <span data-ttu-id="29611-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="29611-134">-SMB</span></span>
<span data-ttu-id="29611-135">AccessProtocol beim Erstellen der Freigabe</span><span class="sxs-lookup"><span data-stu-id="29611-135">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29611-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="29611-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="29611-137">Bereitstellen des Ressourcennamens von StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="29611-137">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29611-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="29611-138">-UserAccessRight</span></span>
<span data-ttu-id="29611-139">Zugriff direkt mit vorhandenen Benutzernamen für den Zugriff auf #A0 bereitstellen, z. B.: @(@{"Benutzername"="Benutzername-1";" AccessRight"="Read"}, @{"Username"="Benutzername-2";" AccessRight"="Read"}, @{"Username"="benutzername-3";" AccessRight"="Benutzerdefiniert"})</span><span class="sxs-lookup"><span data-stu-id="29611-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29611-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29611-140">-Confirm</span></span>
<span data-ttu-id="29611-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29611-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29611-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="29611-142">-WhatIf</span></span>
<span data-ttu-id="29611-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29611-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29611-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29611-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29611-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29611-145">CommonParameters</span></span>
<span data-ttu-id="29611-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29611-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29611-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29611-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29611-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="29611-148">INPUTS</span></span>

### <span data-ttu-id="29611-149">System.String</span><span class="sxs-lookup"><span data-stu-id="29611-149">System.String</span></span>

## <span data-ttu-id="29611-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="29611-150">OUTPUTS</span></span>

### <span data-ttu-id="29611-151">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="29611-151">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="29611-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="29611-152">NOTES</span></span>

## <span data-ttu-id="29611-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="29611-153">RELATED LINKS</span></span>
