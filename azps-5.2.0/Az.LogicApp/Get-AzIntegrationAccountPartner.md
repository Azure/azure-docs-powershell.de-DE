---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
ms.openlocfilehash: cf6d2f4da1803e5c9403803ea7231b55c13d7243
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299688"
---
# <span data-ttu-id="2885d-101">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="2885d-101">Get-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="2885d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2885d-102">SYNOPSIS</span></span>
<span data-ttu-id="2885d-103">Ruft Integrationskontopartner ab.</span><span class="sxs-lookup"><span data-stu-id="2885d-103">Gets integration account partners.</span></span>

## <span data-ttu-id="2885d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2885d-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2885d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2885d-105">DESCRIPTION</span></span>
<span data-ttu-id="2885d-106">Das **Cmdlet "Get-AzIntegrationAccountPartner"** ruft Integrationskontopartner aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="2885d-106">The **Get-AzIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="2885d-107">Geben Sie den Namen des Integrationskontos, den Ressourcengruppennamen und den Partnernamen an.</span><span class="sxs-lookup"><span data-stu-id="2885d-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="2885d-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="2885d-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="2885d-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="2885d-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="2885d-110">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="2885d-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2885d-111">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="2885d-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2885d-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2885d-112">EXAMPLES</span></span>

### <span data-ttu-id="2885d-113">Beispiel 1: Partner für ein Integrationskonto erhalten</span><span class="sxs-lookup"><span data-stu-id="2885d-113">Example 1: Get an integration account partner</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="2885d-114">Dieser Befehl ruft den Integrationskontopartner namens "IntegrationAccountPartner22" ab.</span><span class="sxs-lookup"><span data-stu-id="2885d-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="2885d-115">Beispiel 2: Erhalten eines Integrationskontopartners mithilfe eines Integrationskontonamens</span><span class="sxs-lookup"><span data-stu-id="2885d-115">Example 2: Get an integration account partners by using an integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="2885d-116">Dieser Befehl ruft die Integrationskontopartner für das Integrationskonto namens "IntegrationAccount31" ab.</span><span class="sxs-lookup"><span data-stu-id="2885d-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="2885d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2885d-117">PARAMETERS</span></span>

### <span data-ttu-id="2885d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2885d-118">-DefaultProfile</span></span>
<span data-ttu-id="2885d-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2885d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2885d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2885d-120">-Name</span></span>
<span data-ttu-id="2885d-121">Gibt den Namen eines Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="2885d-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2885d-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="2885d-122">-PartnerName</span></span>
<span data-ttu-id="2885d-123">Gibt den Namen des Integrationskontopartners an.</span><span class="sxs-lookup"><span data-stu-id="2885d-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="2885d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2885d-124">-ResourceGroupName</span></span>
<span data-ttu-id="2885d-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2885d-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2885d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2885d-126">CommonParameters</span></span>
<span data-ttu-id="2885d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2885d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2885d-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2885d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2885d-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2885d-129">INPUTS</span></span>

### <span data-ttu-id="2885d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2885d-130">System.String</span></span>

## <span data-ttu-id="2885d-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2885d-131">OUTPUTS</span></span>

### <span data-ttu-id="2885d-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="2885d-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="2885d-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2885d-133">NOTES</span></span>

## <span data-ttu-id="2885d-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2885d-134">RELATED LINKS</span></span>

[<span data-ttu-id="2885d-135">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="2885d-135">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="2885d-136">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="2885d-136">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="2885d-137">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="2885d-137">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


