---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroup.md
ms.openlocfilehash: 20cfc2ef6b4b59e8cdd605dd14302aa1a172acb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93475934"
---
# <span data-ttu-id="abb9d-101">New-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="abb9d-101">New-AzureRmManagementGroup</span></span>

## <span data-ttu-id="abb9d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="abb9d-102">SYNOPSIS</span></span>
<span data-ttu-id="abb9d-103">Erstellt eine Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="abb9d-103">Creates a Management Group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abb9d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="abb9d-104">SYNTAX</span></span>

### <span data-ttu-id="abb9d-105">GroupOperations (Standard)</span><span class="sxs-lookup"><span data-stu-id="abb9d-105">GroupOperations (Default)</span></span>
```
New-AzureRmManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abb9d-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="abb9d-106">ParentGroupObject</span></span>
```
New-AzureRmManagementGroup [-GroupName] <String> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="abb9d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="abb9d-107">DESCRIPTION</span></span>
<span data-ttu-id="abb9d-108">Das Cmdlet **New-AzureRMManagementGroup** erstellt eine Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="abb9d-108">The **New-AzureRMManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="abb9d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="abb9d-109">EXAMPLES</span></span>

### <span data-ttu-id="abb9d-110">Beispiel 1: Erstellen einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="abb9d-110">Example 1: Create a Management Group</span></span>
```
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="abb9d-111">Erstellen einer neuen Gruppe mit `DisplayName` und " `ParentId` auf" gesetzt `null` .</span><span class="sxs-lookup"><span data-stu-id="abb9d-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="abb9d-112">Das `DisplayName` ist identisch `GroupName` mit dem und das übergeordnete Element der Gruppe ist der Mandant.</span><span class="sxs-lookup"><span data-stu-id="abb9d-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="abb9d-113">Beispiel 2: Erstellen einer Verwaltungsgruppe mit einem Anzeigenamen</span><span class="sxs-lookup"><span data-stu-id="abb9d-113">Example 2: Create a Management Group with a display name</span></span>
```
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="abb9d-114">In diesem Fall ist das übergeordnete Element der Gruppe der Mandant und `DisplayName` wird auf den angegebenen Wert gesetzt.</span><span class="sxs-lookup"><span data-stu-id="abb9d-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="abb9d-115">Beispiel 3: Erstellen einer Verwaltungsgruppe mit einem übergeordneten Element und einem Anzeigenamen</span><span class="sxs-lookup"><span data-stu-id="abb9d-115">Example 3: Create a Management Group with a parent and a display name</span></span>
```
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="abb9d-116">Beispiel 4: Erstellen einer Verwaltungsgruppe mit einem übergeordneten Element (mit einem übergeordneten Objekt)</span><span class="sxs-lookup"><span data-stu-id="abb9d-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
```
PS C:\> $parentObject = Get-AzureRmManagementGroup -GroupName "TestGroupParent"
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

## <span data-ttu-id="abb9d-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="abb9d-117">PARAMETERS</span></span>

### <span data-ttu-id="abb9d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abb9d-118">-DefaultProfile</span></span>
<span data-ttu-id="abb9d-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="abb9d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb9d-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="abb9d-120">-DisplayName</span></span>
<span data-ttu-id="abb9d-121">Anzeige Name der Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="abb9d-121">Display Name of the management group</span></span>

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

### <span data-ttu-id="abb9d-122">-GroupName</span><span class="sxs-lookup"><span data-stu-id="abb9d-122">-GroupName</span></span>
<span data-ttu-id="abb9d-123">Verwaltungsgruppen-ID</span><span class="sxs-lookup"><span data-stu-id="abb9d-123">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb9d-124">-Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="abb9d-124">-ParentId</span></span>
<span data-ttu-id="abb9d-125">Übergeordnete ID der Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="abb9d-125">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb9d-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="abb9d-126">-ParentObject</span></span>
<span data-ttu-id="abb9d-127">Übergeordnetes Objekt</span><span class="sxs-lookup"><span data-stu-id="abb9d-127">Parent Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb9d-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="abb9d-128">-Confirm</span></span>
<span data-ttu-id="abb9d-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="abb9d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abb9d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abb9d-130">-WhatIf</span></span>
<span data-ttu-id="abb9d-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abb9d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abb9d-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="abb9d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abb9d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb9d-133">CommonParameters</span></span>
<span data-ttu-id="abb9d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abb9d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb9d-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abb9d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb9d-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="abb9d-136">INPUTS</span></span>

### <span data-ttu-id="abb9d-137">Keine</span><span class="sxs-lookup"><span data-stu-id="abb9d-137">None</span></span>

## <span data-ttu-id="abb9d-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="abb9d-138">OUTPUTS</span></span>

### <span data-ttu-id="abb9d-139">Microsoft. Azure. Commands. resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="abb9d-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="abb9d-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="abb9d-140">NOTES</span></span>

## <span data-ttu-id="abb9d-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="abb9d-141">RELATED LINKS</span></span>

[<span data-ttu-id="abb9d-142">Remove-AzureRMManagementGroup</span><span class="sxs-lookup"><span data-stu-id="abb9d-142">Remove-AzureRMManagementGroup</span></span>](./Remove-AzureRMManagementGroup.md)

[<span data-ttu-id="abb9d-143">Update-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="abb9d-143">Update-AzureRmManagementGroup</span></span>](./Update-AzureRmManagementGroup.md)

[<span data-ttu-id="abb9d-144">Get-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="abb9d-144">Get-AzureRmManagementGroup</span></span>](./Get-AzureRmManagementGroup.md)
