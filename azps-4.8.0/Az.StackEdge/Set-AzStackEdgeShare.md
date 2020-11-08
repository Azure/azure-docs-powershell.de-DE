---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
ms.openlocfilehash: 2b6c5d5f2295398975d912521ff6d0f001bbd3a2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173405"
---
# <span data-ttu-id="1dbc5-101">Set-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="1dbc5-101">Set-AzStackEdgeShare</span></span>

## <span data-ttu-id="1dbc5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1dbc5-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbc5-103">Aktualisiert die Freigabe für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="1dbc5-103">Updates the share for a device.</span></span>

## <span data-ttu-id="1dbc5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dbc5-104">SYNTAX</span></span>

### <span data-ttu-id="1dbc5-105">SmbParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1dbc5-105">SmbParameterSet (Default)</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1dbc5-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dbc5-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dbc5-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dbc5-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dbc5-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dbc5-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dbc5-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dbc5-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dbc5-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dbc5-110">NfsParameterSet</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1dbc5-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1dbc5-111">DESCRIPTION</span></span>
<span data-ttu-id="1dbc5-112">Dieser **Satz-AzStackEdgeShare** ersetzt die Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="1dbc5-112">This **Set-AzStackEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="1dbc5-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1dbc5-113">EXAMPLES</span></span>

### <span data-ttu-id="1dbc5-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1dbc5-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="1dbc5-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1dbc5-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="1dbc5-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="1dbc5-116">PARAMETERS</span></span>

### <span data-ttu-id="1dbc5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dbc5-117">-AsJob</span></span>
<span data-ttu-id="1dbc5-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1dbc5-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1dbc5-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="1dbc5-119">-ClientAccessRight</span></span>
<span data-ttu-id="1dbc5-120">Lese-/Schreibzugriff für clientIds, für Ex: @ (@ {"ClientID" = "192.168.10.10"; " AccessRight "=" NoAccess "}, @ {" ClientID "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="1dbc5-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="1dbc5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbc5-121">-DefaultProfile</span></span>
<span data-ttu-id="1dbc5-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1dbc5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dbc5-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1dbc5-123">-DeviceName</span></span>
<span data-ttu-id="1dbc5-124">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="1dbc5-124">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbc5-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1dbc5-125">-InputObject</span></span>
<span data-ttu-id="1dbc5-126">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="1dbc5-126">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: UpdateByInputObjectSmbParameterSet, UpdateByInputObjectNfsParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbc5-127">-Name</span><span class="sxs-lookup"><span data-stu-id="1dbc5-127">-Name</span></span>
<span data-ttu-id="1dbc5-128">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="1dbc5-128">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbc5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dbc5-129">-ResourceGroupName</span></span>
<span data-ttu-id="1dbc5-130">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="1dbc5-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbc5-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1dbc5-131">-ResourceId</span></span>
<span data-ttu-id="1dbc5-132">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="1dbc5-132">Azure ResourceId</span></span>

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

### <span data-ttu-id="1dbc5-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="1dbc5-133">-UserAccessRight</span></span>
<span data-ttu-id="1dbc5-134">Bereitstellen des Zugriffsrechts zusammen mit vorhandenen Benutzernamen für den Zugriff auf SMB-Freigabe Typen für Ex: @ (@ {"username" = "User-Name-1"; " AccessRight "=" Read "}, @ {" username "=" User-Name-2 ";" AccessRight "=" Read "}, @ {" username "=" User-Name-3 ";" AccessRight "=" Benutzerdefiniert "})</span><span class="sxs-lookup"><span data-stu-id="1dbc5-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="1dbc5-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1dbc5-135">-Confirm</span></span>
<span data-ttu-id="1dbc5-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1dbc5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dbc5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dbc5-137">-WhatIf</span></span>
<span data-ttu-id="1dbc5-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1dbc5-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1dbc5-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1dbc5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dbc5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbc5-140">CommonParameters</span></span>
<span data-ttu-id="1dbc5-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dbc5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbc5-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1dbc5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbc5-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1dbc5-143">INPUTS</span></span>

### <span data-ttu-id="1dbc5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="1dbc5-144">System.String</span></span>

### <span data-ttu-id="1dbc5-145">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="1dbc5-145">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="1dbc5-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1dbc5-146">OUTPUTS</span></span>

### <span data-ttu-id="1dbc5-147">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="1dbc5-147">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="1dbc5-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="1dbc5-148">NOTES</span></span>

## <span data-ttu-id="1dbc5-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1dbc5-149">RELATED LINKS</span></span>
