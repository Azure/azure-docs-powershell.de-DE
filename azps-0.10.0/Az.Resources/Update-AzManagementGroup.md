---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-Azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzManagementGroup.md
ms.openlocfilehash: cc65c4b4d7d4cc9cf73d3abdf135fd985f71efd6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843140"
---
# <span data-ttu-id="8c3d4-101">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8c3d4-101">Update-AzManagementGroup</span></span>

## <span data-ttu-id="8c3d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8c3d4-102">SYNOPSIS</span></span>
<span data-ttu-id="8c3d4-103">Aktualisiert eine Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="8c3d4-103">Updates a Management Group</span></span>

## <span data-ttu-id="8c3d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c3d4-104">SYNTAX</span></span>

### <span data-ttu-id="8c3d4-105">GroupOperations (Standard)</span><span class="sxs-lookup"><span data-stu-id="8c3d4-105">GroupOperations (Default)</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c3d4-106">ParentAndManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="8c3d4-106">ParentAndManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c3d4-107">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="8c3d4-107">ManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c3d4-108">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="8c3d4-108">ParentGroupObject</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c3d4-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c3d4-109">DESCRIPTION</span></span>
<span data-ttu-id="8c3d4-110">Das Cmdlet **Update-AzManagementGroup** aktualisiert die **übergeordnete** oder **DisplayName** -Datei für eine Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="8c3d4-110">The **Update-AzManagementGroup** cmdlet updates the **ParentId** or **DisplayName** for a Management Group.</span></span>

## <span data-ttu-id="8c3d4-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c3d4-111">EXAMPLES</span></span>

### <span data-ttu-id="8c3d4-112">Beispiel 1: Aktualisieren des Anzeigenamens einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="8c3d4-112">Example 1: Update a Management Group's Display Name</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -DisplayName "New Display Name"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : New Display Name
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
```

### <span data-ttu-id="8c3d4-113">Beispiel 2: Aktualisieren des übergeordneten Elements einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="8c3d4-113">Example 2: Update a Management Group's Parent</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="8c3d4-114">Beispiel 3: Aktualisieren einer Verwaltungsgruppe nach Piping PSManagementGroup-Objekt</span><span class="sxs-lookup"><span data-stu-id="8c3d4-114">Example 3: Update a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Update-AzManagementGroup -DisplayName "TestDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestDisplayName
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="8c3d4-115">Beispiel 4: Aktualisieren des übergeordneten Elements einer Verwaltungsgruppe mit dem übergeordneten Objekt</span><span class="sxs-lookup"><span data-stu-id="8c3d4-115">Example 4: Update a Management Group's parent using the ParentObject</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> Update-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

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

## <span data-ttu-id="8c3d4-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c3d4-116">PARAMETERS</span></span>

### <span data-ttu-id="8c3d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c3d4-117">-DefaultProfile</span></span>
<span data-ttu-id="8c3d4-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8c3d4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c3d4-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8c3d4-119">-DisplayName</span></span>
<span data-ttu-id="8c3d4-120">Anzeige Name der Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="8c3d4-120">Display Name of the management group</span></span>

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

### <span data-ttu-id="8c3d4-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="8c3d4-121">-GroupName</span></span>
<span data-ttu-id="8c3d4-122">Verwaltungsgruppen-ID</span><span class="sxs-lookup"><span data-stu-id="8c3d4-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c3d4-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8c3d4-123">-InputObject</span></span>
<span data-ttu-id="8c3d4-124">Eingabeobjekt aus dem Get-Anruf</span><span class="sxs-lookup"><span data-stu-id="8c3d4-124">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3d4-125">-Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8c3d4-125">-ParentId</span></span>
<span data-ttu-id="8c3d4-126">Übergeordnete ID der Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="8c3d4-126">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ManagementGroupObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c3d4-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8c3d4-127">-ParentObject</span></span>
<span data-ttu-id="8c3d4-128">Eingabeobjekt aus dem Get-Anruf</span><span class="sxs-lookup"><span data-stu-id="8c3d4-128">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c3d4-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8c3d4-129">-Confirm</span></span>
<span data-ttu-id="8c3d4-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c3d4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c3d4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c3d4-131">-WhatIf</span></span>
<span data-ttu-id="8c3d4-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c3d4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c3d4-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c3d4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c3d4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c3d4-134">CommonParameters</span></span>
<span data-ttu-id="8c3d4-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c3d4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c3d4-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c3d4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c3d4-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8c3d4-137">INPUTS</span></span>

### <span data-ttu-id="8c3d4-138">Microsoft. Azure. Commands. resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8c3d4-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>
<span data-ttu-id="8c3d4-139">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8c3d4-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="8c3d4-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8c3d4-140">OUTPUTS</span></span>

### <span data-ttu-id="8c3d4-141">Microsoft. Azure. Commands. resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8c3d4-141">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="8c3d4-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="8c3d4-142">NOTES</span></span>

## <span data-ttu-id="8c3d4-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8c3d4-143">RELATED LINKS</span></span>
