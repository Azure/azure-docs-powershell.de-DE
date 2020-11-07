---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 9991829a70029366086a58020aa53f839db8b6c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658386"
---
# <span data-ttu-id="51e53-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="51e53-101">Update-AzActionRule</span></span>

## <span data-ttu-id="51e53-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="51e53-102">SYNOPSIS</span></span>
<span data-ttu-id="51e53-103">Aktualisiert Aktionsregel Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="51e53-103">Updates action rule properties.</span></span>

## <span data-ttu-id="51e53-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="51e53-104">SYNTAX</span></span>

### <span data-ttu-id="51e53-105">ByNameSimplifiedPatch (Standard)</span><span class="sxs-lookup"><span data-stu-id="51e53-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51e53-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="51e53-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51e53-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="51e53-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51e53-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51e53-108">DESCRIPTION</span></span>
<span data-ttu-id="51e53-109">**Update-AzActionRule** -Cmdlet aktualisiert Aktionsregel Eigenschaften – Status und Kategorien.</span><span class="sxs-lookup"><span data-stu-id="51e53-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="51e53-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51e53-110">EXAMPLES</span></span>

### <span data-ttu-id="51e53-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="51e53-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="51e53-112">Mit diesem Cmdlet wird die Aktionsregel deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="51e53-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="51e53-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="51e53-113">PARAMETERS</span></span>

### <span data-ttu-id="51e53-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51e53-114">-DefaultProfile</span></span>
<span data-ttu-id="51e53-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="51e53-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51e53-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="51e53-116">-InputObject</span></span>
<span data-ttu-id="51e53-117">Die Ressource "Aktionsregel"</span><span class="sxs-lookup"><span data-stu-id="51e53-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51e53-118">-Name</span><span class="sxs-lookup"><span data-stu-id="51e53-118">-Name</span></span>
<span data-ttu-id="51e53-119">Name der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="51e53-119">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e53-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51e53-120">-ResourceGroupName</span></span>
<span data-ttu-id="51e53-121">Name der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="51e53-121">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51e53-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="51e53-122">-ResourceId</span></span>
<span data-ttu-id="51e53-123">Die Ressourcen-ID der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="51e53-123">The resource id of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51e53-124">-Status</span><span class="sxs-lookup"><span data-stu-id="51e53-124">-Status</span></span>
<span data-ttu-id="51e53-125">Aktionsregel Status</span><span class="sxs-lookup"><span data-stu-id="51e53-125">Action rule status</span></span>

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

### <span data-ttu-id="51e53-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="51e53-126">-Tag</span></span>
<span data-ttu-id="51e53-127">Aktionsregel Kategorien</span><span class="sxs-lookup"><span data-stu-id="51e53-127">Action rule tags</span></span>

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

### <span data-ttu-id="51e53-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="51e53-128">-Confirm</span></span>
<span data-ttu-id="51e53-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="51e53-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51e53-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51e53-130">-WhatIf</span></span>
<span data-ttu-id="51e53-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51e53-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51e53-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51e53-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51e53-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e53-133">CommonParameters</span></span>
<span data-ttu-id="51e53-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51e53-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e53-135">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51e53-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e53-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="51e53-136">INPUTS</span></span>

### <span data-ttu-id="51e53-137">System. String</span><span class="sxs-lookup"><span data-stu-id="51e53-137">System.String</span></span>

### <span data-ttu-id="51e53-138">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="51e53-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="51e53-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="51e53-139">OUTPUTS</span></span>

### <span data-ttu-id="51e53-140">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="51e53-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="51e53-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="51e53-141">NOTES</span></span>

## <span data-ttu-id="51e53-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="51e53-142">RELATED LINKS</span></span>
