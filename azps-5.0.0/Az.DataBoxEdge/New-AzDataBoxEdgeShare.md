---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeShare.md
ms.openlocfilehash: 23dcfa42b1b7821e7d2c47b7b3c5e7d7b8579ed6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298762"
---
# <span data-ttu-id="7054b-101">New-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="7054b-101">New-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="7054b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7054b-102">SYNOPSIS</span></span>
<span data-ttu-id="7054b-103">Erstellt eine neue Freigabe auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="7054b-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="7054b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7054b-104">SYNTAX</span></span>

### <span data-ttu-id="7054b-105">SmbParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7054b-105">SmbParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7054b-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="7054b-106">CloudShareNfsParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7054b-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="7054b-107">CloudShareSmbParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7054b-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="7054b-108">NfsParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7054b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7054b-109">DESCRIPTION</span></span>
<span data-ttu-id="7054b-110">Das Cmdlet **New-AzDataBoxEdgeShare** erstellt eine neue Freigabe auf dem Daten Feld-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="7054b-110">The **New-AzDataBoxEdgeShare** cmdlet creates a new share on the Data Box Edge device.</span></span>

## <span data-ttu-id="7054b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7054b-111">EXAMPLES</span></span>

### <span data-ttu-id="7054b-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7054b-112">Example 1</span></span>
```
PS C:\> New-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="7054b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7054b-113">PARAMETERS</span></span>

### <span data-ttu-id="7054b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7054b-114">-AsJob</span></span>
<span data-ttu-id="7054b-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7054b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7054b-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="7054b-116">-ClientAccessRight</span></span>
<span data-ttu-id="7054b-117">Lese-/Schreibzugriff für clientIds, für Ex: @ (@ {"ClientID" = "192.168.10.10"; " AccessRight "=" NoAccess "}, @ {" ClientID "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="7054b-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="7054b-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="7054b-118">-CloudShare</span></span>
<span data-ttu-id="7054b-119">Vorhandenen StorageAccountCredential-Ressourcennamen angeben</span><span class="sxs-lookup"><span data-stu-id="7054b-119">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="7054b-120">-Containername</span><span class="sxs-lookup"><span data-stu-id="7054b-120">-ContainerName</span></span>
<span data-ttu-id="7054b-121">Container Name (auf der Grundlage des angegebenen Datenformats steht dieser Name für Azure files/Pageblob/Block BLOB)</span><span class="sxs-lookup"><span data-stu-id="7054b-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

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

### <span data-ttu-id="7054b-122">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="7054b-122">-DataFormat</span></span>
<span data-ttu-id="7054b-123">Daten Format setzen Ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="7054b-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="7054b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7054b-124">-DefaultProfile</span></span>
<span data-ttu-id="7054b-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7054b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7054b-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7054b-126">-DeviceName</span></span>
<span data-ttu-id="7054b-127">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="7054b-127">Device Name</span></span>

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

### <span data-ttu-id="7054b-128">-Name</span><span class="sxs-lookup"><span data-stu-id="7054b-128">-Name</span></span>
<span data-ttu-id="7054b-129">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="7054b-129">Resource Name</span></span>

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

### <span data-ttu-id="7054b-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="7054b-130">-NFS</span></span>
<span data-ttu-id="7054b-131">AccessProtocol im Fall der Erstellung von Freigabe</span><span class="sxs-lookup"><span data-stu-id="7054b-131">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="7054b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7054b-132">-ResourceGroupName</span></span>
<span data-ttu-id="7054b-133">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="7054b-133">Resource Group Name</span></span>

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

### <span data-ttu-id="7054b-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="7054b-134">-SMB</span></span>
<span data-ttu-id="7054b-135">AccessProtocol im Fall der Erstellung von Freigabe</span><span class="sxs-lookup"><span data-stu-id="7054b-135">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="7054b-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="7054b-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="7054b-137">Vorhandenen StorageAccountCredential-Ressourcennamen angeben</span><span class="sxs-lookup"><span data-stu-id="7054b-137">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="7054b-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="7054b-138">-UserAccessRight</span></span>
<span data-ttu-id="7054b-139">Bereitstellen des Zugriffsrechts zusammen mit vorhandenen Benutzernamen für den Zugriff auf SMB-Freigabe Typen für Ex: @ (@ {"username" = "User-Name-1"; " AccessRight "=" Read "}, @ {" username "=" User-Name-2 ";" AccessRight "=" Read "}, @ {" username "=" User-Name-3 ";" AccessRight "=" Benutzerdefiniert "})</span><span class="sxs-lookup"><span data-stu-id="7054b-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="7054b-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7054b-140">-Confirm</span></span>
<span data-ttu-id="7054b-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7054b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7054b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7054b-142">-WhatIf</span></span>
<span data-ttu-id="7054b-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7054b-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7054b-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7054b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7054b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7054b-145">CommonParameters</span></span>
<span data-ttu-id="7054b-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7054b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7054b-147">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7054b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7054b-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7054b-148">INPUTS</span></span>

### <span data-ttu-id="7054b-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7054b-149">System.String</span></span>

## <span data-ttu-id="7054b-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7054b-150">OUTPUTS</span></span>

### <span data-ttu-id="7054b-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="7054b-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="7054b-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="7054b-152">NOTES</span></span>

## <span data-ttu-id="7054b-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7054b-153">RELATED LINKS</span></span>
