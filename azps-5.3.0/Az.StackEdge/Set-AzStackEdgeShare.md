---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
ms.openlocfilehash: 2b6c5d5f2295398975d912521ff6d0f001bbd3a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374280"
---
# <span data-ttu-id="f6360-101">Set-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f6360-101">Set-AzStackEdgeShare</span></span>

## <span data-ttu-id="f6360-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6360-102">SYNOPSIS</span></span>
<span data-ttu-id="f6360-103">Aktualisiert die Freigabe für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="f6360-103">Updates the share for a device.</span></span>

## <span data-ttu-id="f6360-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6360-104">SYNTAX</span></span>

### <span data-ttu-id="f6360-105">SmbParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6360-105">SmbParameterSet (Default)</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6360-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6360-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6360-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6360-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6360-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6360-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6360-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6360-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6360-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6360-110">NfsParameterSet</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6360-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6360-111">DESCRIPTION</span></span>
<span data-ttu-id="f6360-112">Diese **Set-AzStackEdgeShare** ersetzt die Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="f6360-112">This **Set-AzStackEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="f6360-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f6360-113">EXAMPLES</span></span>

### <span data-ttu-id="f6360-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f6360-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="f6360-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f6360-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="f6360-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6360-116">PARAMETERS</span></span>

### <span data-ttu-id="f6360-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6360-117">-AsJob</span></span>
<span data-ttu-id="f6360-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f6360-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6360-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="f6360-119">-ClientAccessRight</span></span>
<span data-ttu-id="f6360-120">Lese-/Schreibzugriff für clientIds, Für ex:@(@{"ClientId"="192.168.10.10";" AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";" AccessRight"="ReadOnly"})</span><span class="sxs-lookup"><span data-stu-id="f6360-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="f6360-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6360-121">-DefaultProfile</span></span>
<span data-ttu-id="f6360-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6360-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6360-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f6360-123">-DeviceName</span></span>
<span data-ttu-id="f6360-124">Gerätename</span><span class="sxs-lookup"><span data-stu-id="f6360-124">Device Name</span></span>

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

### <span data-ttu-id="f6360-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6360-125">-InputObject</span></span>
<span data-ttu-id="f6360-126">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="f6360-126">Input Object</span></span>

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

### <span data-ttu-id="f6360-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f6360-127">-Name</span></span>
<span data-ttu-id="f6360-128">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="f6360-128">Resource Name</span></span>

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

### <span data-ttu-id="f6360-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6360-129">-ResourceGroupName</span></span>
<span data-ttu-id="f6360-130">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f6360-130">Resource Group Name</span></span>

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

### <span data-ttu-id="f6360-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6360-131">-ResourceId</span></span>
<span data-ttu-id="f6360-132">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6360-132">Azure ResourceId</span></span>

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

### <span data-ttu-id="f6360-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="f6360-133">-UserAccessRight</span></span>
<span data-ttu-id="f6360-134">Zugriff direkt mit vorhandenen Benutzernamen für den Zugriff auf #A0 ermöglichen, z. B.: @(@{"Benutzername"="Benutzername-1";" AccessRight"="Read"}, @{"Username"="Benutzername-2";" AccessRight"="Read"}, @{"Username"="Benutzername-3";" AccessRight"="Custom"})</span><span class="sxs-lookup"><span data-stu-id="f6360-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="f6360-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6360-135">-Confirm</span></span>
<span data-ttu-id="f6360-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6360-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6360-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f6360-137">-WhatIf</span></span>
<span data-ttu-id="f6360-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6360-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6360-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6360-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6360-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6360-140">CommonParameters</span></span>
<span data-ttu-id="f6360-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6360-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6360-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6360-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6360-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f6360-143">INPUTS</span></span>

### <span data-ttu-id="f6360-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f6360-144">System.String</span></span>

### <span data-ttu-id="f6360-145">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f6360-145">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="f6360-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f6360-146">OUTPUTS</span></span>

### <span data-ttu-id="f6360-147">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f6360-147">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="f6360-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f6360-148">NOTES</span></span>

## <span data-ttu-id="f6360-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f6360-149">RELATED LINKS</span></span>
