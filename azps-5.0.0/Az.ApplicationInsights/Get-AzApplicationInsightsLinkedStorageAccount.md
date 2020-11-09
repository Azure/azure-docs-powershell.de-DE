---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 7e879cd4e513ebdad297933269e373c625f2e407
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300868"
---
# <span data-ttu-id="36cc6-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36cc6-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="36cc6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="36cc6-103">Abrufen des verknüpften speicherkontos für Application Insights</span><span class="sxs-lookup"><span data-stu-id="36cc6-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="36cc6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36cc6-104">SYNTAX</span></span>

### <span data-ttu-id="36cc6-105">ByResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="36cc6-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36cc6-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36cc6-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36cc6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36cc6-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36cc6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36cc6-108">DESCRIPTION</span></span>
<span data-ttu-id="36cc6-109">Abrufen des verknüpften speicherkontos für Application Insights</span><span class="sxs-lookup"><span data-stu-id="36cc6-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="36cc6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36cc6-110">EXAMPLES</span></span>

### <span data-ttu-id="36cc6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="36cc6-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="36cc6-112">Abrufen des verknüpften speicherkontos, das der Komponente "Komponentenname" zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="36cc6-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="36cc6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="36cc6-113">PARAMETERS</span></span>

### <span data-ttu-id="36cc6-114">-Komponentenname</span><span class="sxs-lookup"><span data-stu-id="36cc6-114">-ComponentName</span></span>
<span data-ttu-id="36cc6-115">Komponenten Name</span><span class="sxs-lookup"><span data-stu-id="36cc6-115">Component Name</span></span>

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

### <span data-ttu-id="36cc6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36cc6-116">-DefaultProfile</span></span>
<span data-ttu-id="36cc6-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="36cc6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36cc6-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="36cc6-118">-InputObject</span></span>
<span data-ttu-id="36cc6-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="36cc6-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="36cc6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36cc6-120">-ResourceGroupName</span></span>
<span data-ttu-id="36cc6-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="36cc6-121">Resource Group Name</span></span>

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

### <span data-ttu-id="36cc6-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="36cc6-122">-ResourceId</span></span>
<span data-ttu-id="36cc6-123">Komponenten-wiederherkunfts-Nr</span><span class="sxs-lookup"><span data-stu-id="36cc6-123">Component ResourceId</span></span>

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

### <span data-ttu-id="36cc6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36cc6-124">CommonParameters</span></span>
<span data-ttu-id="36cc6-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36cc6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36cc6-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36cc6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36cc6-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36cc6-127">INPUTS</span></span>

### <span data-ttu-id="36cc6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="36cc6-128">System.String</span></span>

### <span data-ttu-id="36cc6-129">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="36cc6-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="36cc6-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36cc6-130">OUTPUTS</span></span>

### <span data-ttu-id="36cc6-131">Microsoft. Azure. Commands. ApplicationInsights. Models. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="36cc6-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="36cc6-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="36cc6-132">NOTES</span></span>

## <span data-ttu-id="36cc6-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36cc6-133">RELATED LINKS</span></span>
