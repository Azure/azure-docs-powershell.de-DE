---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 2af687a79255d5e5ab4b49135bf8a8f7b8f819f1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995894"
---
# <span data-ttu-id="bbd5c-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="bbd5c-101">Update-AzActionRule</span></span>

## <span data-ttu-id="bbd5c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bbd5c-102">SYNOPSIS</span></span>
<span data-ttu-id="bbd5c-103">Aktualisiert Aktionsregel Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bbd5c-103">Updates action rule properties.</span></span>

## <span data-ttu-id="bbd5c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbd5c-104">SYNTAX</span></span>

### <span data-ttu-id="bbd5c-105">ByNameSimplifiedPatch (Standard)</span><span class="sxs-lookup"><span data-stu-id="bbd5c-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbd5c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bbd5c-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbd5c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bbd5c-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbd5c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bbd5c-108">DESCRIPTION</span></span>
<span data-ttu-id="bbd5c-109">**Update-AzActionRule** -Cmdlet aktualisiert Aktionsregel Eigenschaften – Status und Kategorien.</span><span class="sxs-lookup"><span data-stu-id="bbd5c-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="bbd5c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bbd5c-110">EXAMPLES</span></span>

### <span data-ttu-id="bbd5c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bbd5c-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="bbd5c-112">Mit diesem Cmdlet wird die Aktionsregel deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bbd5c-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="bbd5c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="bbd5c-113">PARAMETERS</span></span>

### <span data-ttu-id="bbd5c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbd5c-114">-DefaultProfile</span></span>
<span data-ttu-id="bbd5c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bbd5c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbd5c-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bbd5c-116">-InputObject</span></span>
<span data-ttu-id="bbd5c-117">Die Ressource "Aktionsregel"</span><span class="sxs-lookup"><span data-stu-id="bbd5c-117">The action rule resource</span></span>

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

### <span data-ttu-id="bbd5c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bbd5c-118">-Name</span></span>
<span data-ttu-id="bbd5c-119">Name der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="bbd5c-119">Action rule name</span></span>

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

### <span data-ttu-id="bbd5c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbd5c-120">-ResourceGroupName</span></span>
<span data-ttu-id="bbd5c-121">Name der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="bbd5c-121">Action rule name</span></span>

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

### <span data-ttu-id="bbd5c-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="bbd5c-122">-ResourceId</span></span>
<span data-ttu-id="bbd5c-123">Die Ressourcen-ID der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="bbd5c-123">The resource id of action rule</span></span>

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

### <span data-ttu-id="bbd5c-124">-Status</span><span class="sxs-lookup"><span data-stu-id="bbd5c-124">-Status</span></span>
<span data-ttu-id="bbd5c-125">Aktionsregel Status</span><span class="sxs-lookup"><span data-stu-id="bbd5c-125">Action rule status</span></span>

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

### <span data-ttu-id="bbd5c-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="bbd5c-126">-Tag</span></span>
<span data-ttu-id="bbd5c-127">Aktionsregel Kategorien</span><span class="sxs-lookup"><span data-stu-id="bbd5c-127">Action rule tags</span></span>

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

### <span data-ttu-id="bbd5c-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bbd5c-128">-Confirm</span></span>
<span data-ttu-id="bbd5c-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bbd5c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbd5c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbd5c-130">-WhatIf</span></span>
<span data-ttu-id="bbd5c-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bbd5c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbd5c-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bbd5c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbd5c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbd5c-133">CommonParameters</span></span>
<span data-ttu-id="bbd5c-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbd5c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbd5c-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbd5c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbd5c-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bbd5c-136">INPUTS</span></span>

### <span data-ttu-id="bbd5c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="bbd5c-137">System.String</span></span>

### <span data-ttu-id="bbd5c-138">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="bbd5c-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="bbd5c-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bbd5c-139">OUTPUTS</span></span>

### <span data-ttu-id="bbd5c-140">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="bbd5c-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="bbd5c-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="bbd5c-141">NOTES</span></span>

## <span data-ttu-id="bbd5c-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bbd5c-142">RELATED LINKS</span></span>
