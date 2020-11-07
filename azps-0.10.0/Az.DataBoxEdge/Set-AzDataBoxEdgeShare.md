---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
ms.openlocfilehash: ac4f7814898bcbfcee75c4a31273dfbcb6be7335
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842403"
---
# <span data-ttu-id="aa816-101">Set-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="aa816-101">Set-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="aa816-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aa816-102">SYNOPSIS</span></span>
<span data-ttu-id="aa816-103">Aktualisiert die Freigabe für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="aa816-103">Updates the share for a device.</span></span>

## <span data-ttu-id="aa816-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa816-104">SYNTAX</span></span>

### <span data-ttu-id="aa816-105">SmbParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="aa816-105">SmbParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa816-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa816-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa816-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa816-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa816-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa816-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa816-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa816-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa816-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa816-110">NfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa816-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa816-111">DESCRIPTION</span></span>
<span data-ttu-id="aa816-112">Dieser **Satz-AzDataBoxEdgeShare** ersetzt die Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="aa816-112">This **Set-AzDataBoxEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="aa816-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa816-113">EXAMPLES</span></span>

### <span data-ttu-id="aa816-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aa816-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="aa816-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="aa816-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="aa816-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa816-116">PARAMETERS</span></span>

### <span data-ttu-id="aa816-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa816-117">-AsJob</span></span>
<span data-ttu-id="aa816-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="aa816-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa816-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="aa816-119">-ClientAccessRight</span></span>
<span data-ttu-id="aa816-120">Lese-/Schreibzugriff für clientIds, für Ex: @ (@ {"ClientID" = "192.168.10.10"; " AccessRight "=" NoAccess "}, @ {" ClientID "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="aa816-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: UpdateByResourceIdNfsParameterSet, UpdateByInputObjectNfsParameterSet, NfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa816-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa816-121">-DefaultProfile</span></span>
<span data-ttu-id="aa816-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aa816-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa816-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="aa816-123">-DeviceName</span></span>
<span data-ttu-id="aa816-124">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="aa816-124">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa816-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aa816-125">-InputObject</span></span>
<span data-ttu-id="aa816-126">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="aa816-126">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: UpdateByInputObjectSmbParameterSet, UpdateByInputObjectNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa816-127">-Name</span><span class="sxs-lookup"><span data-stu-id="aa816-127">-Name</span></span>
<span data-ttu-id="aa816-128">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="aa816-128">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa816-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa816-129">-ResourceGroupName</span></span>
<span data-ttu-id="aa816-130">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="aa816-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa816-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="aa816-131">-ResourceId</span></span>
<span data-ttu-id="aa816-132">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="aa816-132">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdSmbParameterSet, UpdateByResourceIdNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa816-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="aa816-133">-UserAccessRight</span></span>
<span data-ttu-id="aa816-134">Bereitstellen des Zugriffsrechts zusammen mit vorhandenen Benutzernamen für den Zugriff auf SMB-Freigabe Typen für Ex: @ (@ {"username" = "User-Name-1"; " AccessRight "=" Read "}, @ {" username "=" User-Name-2 ";" AccessRight "=" Read "}, @ {" username "=" User-Name-3 ";" AccessRight "=" Benutzerdefiniert "})</span><span class="sxs-lookup"><span data-stu-id="aa816-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, UpdateByResourceIdSmbParameterSet, UpdateByInputObjectSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa816-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aa816-135">-Confirm</span></span>
<span data-ttu-id="aa816-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa816-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa816-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa816-137">-WhatIf</span></span>
<span data-ttu-id="aa816-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa816-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa816-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa816-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa816-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa816-140">CommonParameters</span></span>
<span data-ttu-id="aa816-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa816-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa816-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa816-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa816-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aa816-143">INPUTS</span></span>

### <span data-ttu-id="aa816-144">System. String</span><span class="sxs-lookup"><span data-stu-id="aa816-144">System.String</span></span>

### <span data-ttu-id="aa816-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="aa816-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="aa816-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aa816-146">OUTPUTS</span></span>

### <span data-ttu-id="aa816-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="aa816-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="aa816-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="aa816-148">NOTES</span></span>

## <span data-ttu-id="aa816-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aa816-149">RELATED LINKS</span></span>
