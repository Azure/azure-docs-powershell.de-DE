---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 652a5668bd641ae1b68093f431e0aa0963aca50b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178351"
---
# <span data-ttu-id="26951-101">New-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="26951-101">New-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="26951-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26951-102">SYNOPSIS</span></span>
<span data-ttu-id="26951-103">Erstellen eines verknüpften speicherkontos für Application Insights</span><span class="sxs-lookup"><span data-stu-id="26951-103">Create an application insights linked storage account</span></span>

## <span data-ttu-id="26951-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26951-104">SYNTAX</span></span>

### <span data-ttu-id="26951-105">ByResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="26951-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26951-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26951-106">ByInputObjectParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26951-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26951-107">ByResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26951-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26951-108">DESCRIPTION</span></span>
<span data-ttu-id="26951-109">Erstellen eines verknüpften speicherkontos für Application Insights</span><span class="sxs-lookup"><span data-stu-id="26951-109">Create an application insights linked storage account</span></span>

## <span data-ttu-id="26951-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26951-110">EXAMPLES</span></span>

### <span data-ttu-id="26951-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="26951-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | New-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="26951-112">Erstellen eines verknüpften speicherkontos $Account Unterkomponente "Komponentenname"</span><span class="sxs-lookup"><span data-stu-id="26951-112">Create linked storage account $account under component "componentName"</span></span>

## <span data-ttu-id="26951-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="26951-113">PARAMETERS</span></span>

### <span data-ttu-id="26951-114">-Komponentenname</span><span class="sxs-lookup"><span data-stu-id="26951-114">-ComponentName</span></span>
<span data-ttu-id="26951-115">Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="26951-115">Component Name</span></span>

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

### <span data-ttu-id="26951-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26951-116">-DefaultProfile</span></span>
<span data-ttu-id="26951-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="26951-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26951-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="26951-118">-InputObject</span></span>
<span data-ttu-id="26951-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="26951-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="26951-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="26951-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="26951-121">Speicherkonto-wiederherkunfts-Nr</span><span class="sxs-lookup"><span data-stu-id="26951-121">Storage Account ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26951-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26951-122">-ResourceGroupName</span></span>
<span data-ttu-id="26951-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="26951-123">Resource Group Name</span></span>

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

### <span data-ttu-id="26951-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="26951-124">-ResourceId</span></span>
<span data-ttu-id="26951-125">Komponenten-wiederherkunfts-Nr</span><span class="sxs-lookup"><span data-stu-id="26951-125">Component ResourceId</span></span>

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

### <span data-ttu-id="26951-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="26951-126">-Confirm</span></span>
<span data-ttu-id="26951-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="26951-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26951-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26951-128">-WhatIf</span></span>
<span data-ttu-id="26951-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26951-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26951-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26951-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26951-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26951-131">CommonParameters</span></span>
<span data-ttu-id="26951-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26951-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26951-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26951-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26951-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26951-134">INPUTS</span></span>

### <span data-ttu-id="26951-135">System. String</span><span class="sxs-lookup"><span data-stu-id="26951-135">System.String</span></span>

### <span data-ttu-id="26951-136">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="26951-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="26951-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26951-137">OUTPUTS</span></span>

### <span data-ttu-id="26951-138">Microsoft. Azure. Commands. ApplicationInsights. Models. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="26951-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="26951-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="26951-139">NOTES</span></span>

## <span data-ttu-id="26951-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26951-140">RELATED LINKS</span></span>
