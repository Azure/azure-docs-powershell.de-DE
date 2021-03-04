---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeShare.md
ms.openlocfilehash: bfccf106d2dbc541f9887fddff12bd512640f55c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931920"
---
# <span data-ttu-id="971a3-101">New-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="971a3-101">New-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="971a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="971a3-102">SYNOPSIS</span></span>
<span data-ttu-id="971a3-103">Erstellt eine neue Freigabe auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="971a3-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="971a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="971a3-104">SYNTAX</span></span>

### <span data-ttu-id="971a3-105">SmbParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="971a3-105">SmbParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="971a3-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="971a3-106">CloudShareNfsParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="971a3-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="971a3-107">CloudShareSmbParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="971a3-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="971a3-108">NfsParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="971a3-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="971a3-109">DESCRIPTION</span></span>
<span data-ttu-id="971a3-110">Das **New-AzDataBoxEdgeShare-Cmdlet** erstellt eine neue Freigabe auf dem Data Box Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="971a3-110">The **New-AzDataBoxEdgeShare** cmdlet creates a new share on the Data Box Edge device.</span></span>

## <span data-ttu-id="971a3-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="971a3-111">EXAMPLES</span></span>

### <span data-ttu-id="971a3-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="971a3-112">Example 1</span></span>
```
PS C:\> New-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="971a3-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="971a3-113">PARAMETERS</span></span>

### <span data-ttu-id="971a3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="971a3-114">-AsJob</span></span>
<span data-ttu-id="971a3-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="971a3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="971a3-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="971a3-116">-ClientAccessRight</span></span>
<span data-ttu-id="971a3-117">Lese-/Schreibzugriff für clientIds, Für ex:@(@{"ClientId"="192.168.10.10";" AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";" AccessRight"="ReadOnly"})</span><span class="sxs-lookup"><span data-stu-id="971a3-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="971a3-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="971a3-118">-CloudShare</span></span>
<span data-ttu-id="971a3-119">Bereitstellen des Ressourcennamens von StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="971a3-119">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="971a3-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="971a3-120">-ContainerName</span></span>
<span data-ttu-id="971a3-121">Containername (Basierend auf dem angegebenen Datenformat stellt dies den Namen von Azure Files/Pageblob/Block blob dar)</span><span class="sxs-lookup"><span data-stu-id="971a3-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

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

### <span data-ttu-id="971a3-122">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="971a3-122">-DataFormat</span></span>
<span data-ttu-id="971a3-123">Festlegen des Datenformats ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="971a3-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="971a3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="971a3-124">-DefaultProfile</span></span>
<span data-ttu-id="971a3-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="971a3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="971a3-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="971a3-126">-DeviceName</span></span>
<span data-ttu-id="971a3-127">Gerätename</span><span class="sxs-lookup"><span data-stu-id="971a3-127">Device Name</span></span>

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

### <span data-ttu-id="971a3-128">-Name</span><span class="sxs-lookup"><span data-stu-id="971a3-128">-Name</span></span>
<span data-ttu-id="971a3-129">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="971a3-129">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971a3-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="971a3-130">-NFS</span></span>
<span data-ttu-id="971a3-131">AccessProtocol beim Erstellen von Freigaben</span><span class="sxs-lookup"><span data-stu-id="971a3-131">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="971a3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="971a3-132">-ResourceGroupName</span></span>
<span data-ttu-id="971a3-133">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="971a3-133">Resource Group Name</span></span>

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

### <span data-ttu-id="971a3-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="971a3-134">-SMB</span></span>
<span data-ttu-id="971a3-135">AccessProtocol beim Erstellen von Freigaben</span><span class="sxs-lookup"><span data-stu-id="971a3-135">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="971a3-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="971a3-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="971a3-137">Bereitstellen des Ressourcennamens von StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="971a3-137">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="971a3-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="971a3-138">-UserAccessRight</span></span>
<span data-ttu-id="971a3-139">Zugriff direkt zusammen mit vorhandenen Benutzernamen für den Zugriff auf #A0 bereitstellen, z. B. @(@{"Benutzername"="Benutzername-1";" AccessRight"="Read"}, @{"Benutzername"="Benutzername-2";" AccessRight"="Read"}, @{"Benutzername"="Benutzername-3";" AccessRight"="Custom"})</span><span class="sxs-lookup"><span data-stu-id="971a3-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="971a3-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="971a3-140">-Confirm</span></span>
<span data-ttu-id="971a3-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="971a3-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="971a3-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="971a3-142">-WhatIf</span></span>
<span data-ttu-id="971a3-143">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="971a3-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="971a3-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="971a3-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="971a3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="971a3-145">CommonParameters</span></span>
<span data-ttu-id="971a3-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="971a3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="971a3-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="971a3-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="971a3-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="971a3-148">INPUTS</span></span>

### <span data-ttu-id="971a3-149">System.String</span><span class="sxs-lookup"><span data-stu-id="971a3-149">System.String</span></span>

## <span data-ttu-id="971a3-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="971a3-150">OUTPUTS</span></span>

### <span data-ttu-id="971a3-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="971a3-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="971a3-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="971a3-152">NOTES</span></span>

## <span data-ttu-id="971a3-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="971a3-153">RELATED LINKS</span></span>
