---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
ms.openlocfilehash: cf6d2f4da1803e5c9403803ea7231b55c13d7243
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180374"
---
# <span data-ttu-id="6c2c0-101">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="6c2c0-101">Get-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="6c2c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c2c0-102">SYNOPSIS</span></span>
<span data-ttu-id="6c2c0-103">Ruft Integrations Kontopartner ab.</span><span class="sxs-lookup"><span data-stu-id="6c2c0-103">Gets integration account partners.</span></span>

## <span data-ttu-id="6c2c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c2c0-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c2c0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c2c0-105">DESCRIPTION</span></span>
<span data-ttu-id="6c2c0-106">Das Cmdlet " **Get-AzIntegrationAccountPartner** " ruft Integrations Kontopartner aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="6c2c0-106">The **Get-AzIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="6c2c0-107">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Partnernamen an.</span><span class="sxs-lookup"><span data-stu-id="6c2c0-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="6c2c0-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="6c2c0-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6c2c0-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="6c2c0-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6c2c0-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="6c2c0-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6c2c0-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="6c2c0-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6c2c0-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c2c0-112">EXAMPLES</span></span>

### <span data-ttu-id="6c2c0-113">Beispiel 1: Abrufen eines Integrations Kontopartners</span><span class="sxs-lookup"><span data-stu-id="6c2c0-113">Example 1: Get an integration account partner</span></span>
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

<span data-ttu-id="6c2c0-114">Dieser Befehl ruft den Integrations Kontopartner mit dem Namen IntegrationAccountPartner22 ab.</span><span class="sxs-lookup"><span data-stu-id="6c2c0-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="6c2c0-115">Beispiel 2: Abrufen eines Integrations Kontopartners mithilfe eines Integrations Kontonamens</span><span class="sxs-lookup"><span data-stu-id="6c2c0-115">Example 2: Get an integration account partners by using an integration account name</span></span>
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

<span data-ttu-id="6c2c0-116">Dieser Befehl ruft die Integrations Kontopartner für das Integrations Konto mit dem Namen IntegrationAccount31 ab.</span><span class="sxs-lookup"><span data-stu-id="6c2c0-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="6c2c0-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c2c0-117">PARAMETERS</span></span>

### <span data-ttu-id="6c2c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c2c0-118">-DefaultProfile</span></span>
<span data-ttu-id="6c2c0-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6c2c0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c2c0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6c2c0-120">-Name</span></span>
<span data-ttu-id="6c2c0-121">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="6c2c0-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="6c2c0-122">-Partnername</span><span class="sxs-lookup"><span data-stu-id="6c2c0-122">-PartnerName</span></span>
<span data-ttu-id="6c2c0-123">Gibt den Namen des Integrations Kontopartners an.</span><span class="sxs-lookup"><span data-stu-id="6c2c0-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="6c2c0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c2c0-124">-ResourceGroupName</span></span>
<span data-ttu-id="6c2c0-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6c2c0-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6c2c0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c2c0-126">CommonParameters</span></span>
<span data-ttu-id="6c2c0-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c2c0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c2c0-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c2c0-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c2c0-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c2c0-129">INPUTS</span></span>

### <span data-ttu-id="6c2c0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6c2c0-130">System.String</span></span>

## <span data-ttu-id="6c2c0-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c2c0-131">OUTPUTS</span></span>

### <span data-ttu-id="6c2c0-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="6c2c0-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="6c2c0-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c2c0-133">NOTES</span></span>

## <span data-ttu-id="6c2c0-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c2c0-134">RELATED LINKS</span></span>

[<span data-ttu-id="6c2c0-135">Neu – AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="6c2c0-135">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="6c2c0-136">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="6c2c0-136">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="6c2c0-137">Satz-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="6c2c0-137">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


