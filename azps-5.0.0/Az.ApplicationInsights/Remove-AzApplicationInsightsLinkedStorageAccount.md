---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 6bb6a422af88c0d7cd911e575e9d49bcdafcd3d8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179925"
---
# <span data-ttu-id="69447-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="69447-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="69447-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="69447-102">SYNOPSIS</span></span>
<span data-ttu-id="69447-103">Löschen eines verknüpften speicherkontos für Application Insights</span><span class="sxs-lookup"><span data-stu-id="69447-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="69447-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="69447-104">SYNTAX</span></span>

### <span data-ttu-id="69447-105">ByResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="69447-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69447-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69447-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69447-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="69447-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69447-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69447-108">DESCRIPTION</span></span>
<span data-ttu-id="69447-109">Löschen eines verknüpften speicherkontos für Application Insights</span><span class="sxs-lookup"><span data-stu-id="69447-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="69447-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69447-110">EXAMPLES</span></span>

### <span data-ttu-id="69447-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="69447-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="69447-112">Löschen eines verknüpften speicherkontos, das mit der Komponente "Komponentenname" der Anwendungs Einsichten verknüpft ist</span><span class="sxs-lookup"><span data-stu-id="69447-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="69447-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="69447-113">PARAMETERS</span></span>

### <span data-ttu-id="69447-114">-Komponentenname</span><span class="sxs-lookup"><span data-stu-id="69447-114">-ComponentName</span></span>
<span data-ttu-id="69447-115">Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="69447-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69447-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69447-116">-DefaultProfile</span></span>
<span data-ttu-id="69447-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="69447-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69447-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="69447-118">-InputObject</span></span>
<span data-ttu-id="69447-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="69447-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69447-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69447-120">-ResourceGroupName</span></span>
<span data-ttu-id="69447-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="69447-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69447-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="69447-122">-ResourceId</span></span>
<span data-ttu-id="69447-123">Komponenten-wiederherkunfts-Nr</span><span class="sxs-lookup"><span data-stu-id="69447-123">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69447-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="69447-124">-Confirm</span></span>
<span data-ttu-id="69447-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69447-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69447-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69447-126">-WhatIf</span></span>
<span data-ttu-id="69447-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69447-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69447-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69447-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69447-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69447-129">CommonParameters</span></span>
<span data-ttu-id="69447-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69447-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69447-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69447-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69447-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="69447-132">INPUTS</span></span>

### <span data-ttu-id="69447-133">System. String</span><span class="sxs-lookup"><span data-stu-id="69447-133">System.String</span></span>

### <span data-ttu-id="69447-134">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="69447-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="69447-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="69447-135">OUTPUTS</span></span>

### <span data-ttu-id="69447-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="69447-136">System.Boolean</span></span>

## <span data-ttu-id="69447-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="69447-137">NOTES</span></span>

## <span data-ttu-id="69447-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="69447-138">RELATED LINKS</span></span>
