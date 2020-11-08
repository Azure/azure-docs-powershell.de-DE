---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 1cdea9a2d5deb9fbe93da0a090070f7ed1b07653
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995899"
---
# <span data-ttu-id="795c5-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="795c5-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="795c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="795c5-102">SYNOPSIS</span></span>
<span data-ttu-id="795c5-103">Löscht eine Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="795c5-103">Deletes a action rule</span></span>

## <span data-ttu-id="795c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="795c5-104">SYNTAX</span></span>

### <span data-ttu-id="795c5-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="795c5-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="795c5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="795c5-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="795c5-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="795c5-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="795c5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="795c5-108">DESCRIPTION</span></span>
<span data-ttu-id="795c5-109">**Remove-AzActionRule-** Cmdlet löscht eine Aktionsregel.</span><span class="sxs-lookup"><span data-stu-id="795c5-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="795c5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="795c5-110">EXAMPLES</span></span>

### <span data-ttu-id="795c5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="795c5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="795c5-112">Dieses Cmdlet löscht die Aktionsregel mit dem Namen ActionRuleName in der Ressourcengruppe Test-RG</span><span class="sxs-lookup"><span data-stu-id="795c5-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="795c5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="795c5-113">PARAMETERS</span></span>

### <span data-ttu-id="795c5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="795c5-114">-DefaultProfile</span></span>
<span data-ttu-id="795c5-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="795c5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="795c5-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="795c5-116">-InputObject</span></span>
<span data-ttu-id="795c5-117">Die Ressource "Aktionsregel"</span><span class="sxs-lookup"><span data-stu-id="795c5-117">The action rule resource</span></span>

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

### <span data-ttu-id="795c5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="795c5-118">-Name</span></span>
<span data-ttu-id="795c5-119">Name der Aktionsregel</span><span class="sxs-lookup"><span data-stu-id="795c5-119">Name of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="795c5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="795c5-120">-PassThru</span></span>
<span data-ttu-id="795c5-121">PassThru gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="795c5-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="795c5-122">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="795c5-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="795c5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="795c5-123">-ResourceGroupName</span></span>
<span data-ttu-id="795c5-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="795c5-124">Resource Group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="795c5-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="795c5-125">-ResourceId</span></span>
<span data-ttu-id="795c5-126">Abrufen einer Aktionsregel nach der Resoure-ID</span><span class="sxs-lookup"><span data-stu-id="795c5-126">Get Action rule by resoure id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="795c5-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="795c5-127">-Confirm</span></span>
<span data-ttu-id="795c5-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="795c5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="795c5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="795c5-129">-WhatIf</span></span>
<span data-ttu-id="795c5-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="795c5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="795c5-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="795c5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="795c5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="795c5-132">CommonParameters</span></span>
<span data-ttu-id="795c5-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="795c5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="795c5-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="795c5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="795c5-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="795c5-135">INPUTS</span></span>

### <span data-ttu-id="795c5-136">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="795c5-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="795c5-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="795c5-137">OUTPUTS</span></span>

### <span data-ttu-id="795c5-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="795c5-138">System.Boolean</span></span>

## <span data-ttu-id="795c5-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="795c5-139">NOTES</span></span>

## <span data-ttu-id="795c5-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="795c5-140">RELATED LINKS</span></span>
