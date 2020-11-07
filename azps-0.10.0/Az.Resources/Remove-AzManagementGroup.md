---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: 9ac7717769cef1ad147ea122ddedde3efd1e389f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843256"
---
# <span data-ttu-id="53c04-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="53c04-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="53c04-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="53c04-102">SYNOPSIS</span></span>
<span data-ttu-id="53c04-103">Entfernt eine Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="53c04-103">Removes a Management Group</span></span>

## <span data-ttu-id="53c04-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="53c04-104">SYNTAX</span></span>

### <span data-ttu-id="53c04-105">GroupOperations (Standard)</span><span class="sxs-lookup"><span data-stu-id="53c04-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53c04-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="53c04-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53c04-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="53c04-107">DESCRIPTION</span></span>
<span data-ttu-id="53c04-108">Das Cmdlet **Remove-AzManagementGroup** löscht eine Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="53c04-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="53c04-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53c04-109">EXAMPLES</span></span>

### <span data-ttu-id="53c04-110">Beispiel 1 – Entfernen einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="53c04-110">Example 1 - Remove a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="53c04-111">Beispiel 2 – Entfernen einer Verwaltungsgruppe durch Piping PSManagementGroup-Objekt</span><span class="sxs-lookup"><span data-stu-id="53c04-111">Example 2 - Remove a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-Remove-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="53c04-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="53c04-112">PARAMETERS</span></span>

### <span data-ttu-id="53c04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53c04-113">-DefaultProfile</span></span>
<span data-ttu-id="53c04-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="53c04-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53c04-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="53c04-115">-GroupName</span></span>
<span data-ttu-id="53c04-116">Verwaltungsgruppen-ID</span><span class="sxs-lookup"><span data-stu-id="53c04-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53c04-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="53c04-117">-InputObject</span></span>
<span data-ttu-id="53c04-118">Eingabeobjekt aus dem Get-Anruf</span><span class="sxs-lookup"><span data-stu-id="53c04-118">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53c04-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53c04-119">-PassThru</span></span>
<span data-ttu-id="53c04-120">Zurück `true` zur erfolgreichen Ausführung</span><span class="sxs-lookup"><span data-stu-id="53c04-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="53c04-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="53c04-121">-Confirm</span></span>
<span data-ttu-id="53c04-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="53c04-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53c04-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53c04-123">-WhatIf</span></span>
<span data-ttu-id="53c04-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="53c04-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53c04-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="53c04-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53c04-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c04-126">CommonParameters</span></span>
<span data-ttu-id="53c04-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53c04-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c04-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53c04-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c04-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="53c04-129">INPUTS</span></span>

### <span data-ttu-id="53c04-130">Microsoft. Azure. Commands. resources. Models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="53c04-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>
<span data-ttu-id="53c04-131">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="53c04-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="53c04-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="53c04-132">OUTPUTS</span></span>

### <span data-ttu-id="53c04-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="53c04-133">System.Boolean</span></span>

## <span data-ttu-id="53c04-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="53c04-134">NOTES</span></span>

## <span data-ttu-id="53c04-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="53c04-135">RELATED LINKS</span></span>
