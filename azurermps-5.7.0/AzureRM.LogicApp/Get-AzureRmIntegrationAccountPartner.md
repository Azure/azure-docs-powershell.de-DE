---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 7063fb81705a14f1c1d8f0d02a2dc51d8a5617ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663476"
---
# <span data-ttu-id="8cdc1-101">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="8cdc1-101">Get-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="8cdc1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8cdc1-102">SYNOPSIS</span></span>
<span data-ttu-id="8cdc1-103">Ruft Integrations Kontopartner ab.</span><span class="sxs-lookup"><span data-stu-id="8cdc1-103">Gets integration account partners.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cdc1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cdc1-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cdc1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cdc1-105">DESCRIPTION</span></span>
<span data-ttu-id="8cdc1-106">Das Cmdlet " **Get-AzureRmIntegrationAccountPartner** " ruft Integrations Kontopartner aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="8cdc1-106">The **Get-AzureRmIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="8cdc1-107">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Partnernamen an.</span><span class="sxs-lookup"><span data-stu-id="8cdc1-107">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="8cdc1-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="8cdc1-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8cdc1-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="8cdc1-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8cdc1-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="8cdc1-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8cdc1-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="8cdc1-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8cdc1-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8cdc1-112">EXAMPLES</span></span>

### <span data-ttu-id="8cdc1-113">Beispiel 1: Abrufen eines Integrations Kontopartners</span><span class="sxs-lookup"><span data-stu-id="8cdc1-113">Example 1: Get an integration account partner</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="8cdc1-114">Dieser Befehl ruft den Integrations Kontopartner mit dem Namen IntegrationAccountPartner22 ab.</span><span class="sxs-lookup"><span data-stu-id="8cdc1-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="8cdc1-115">Beispiel 2: Abrufen eines Integrations Kontopartners mithilfe eines Integrations Kontonamens</span><span class="sxs-lookup"><span data-stu-id="8cdc1-115">Example 2: Get an integration account partners by using an integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="8cdc1-116">Dieser Befehl ruft die Integrations Kontopartner für das Integrations Konto mit dem Namen IntegrationAccount31 ab.</span><span class="sxs-lookup"><span data-stu-id="8cdc1-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="8cdc1-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cdc1-117">PARAMETERS</span></span>

### <span data-ttu-id="8cdc1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cdc1-118">-DefaultProfile</span></span>
<span data-ttu-id="8cdc1-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8cdc1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cdc1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8cdc1-120">-Name</span></span>
<span data-ttu-id="8cdc1-121">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="8cdc1-121">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cdc1-122">-Partnername</span><span class="sxs-lookup"><span data-stu-id="8cdc1-122">-PartnerName</span></span>
<span data-ttu-id="8cdc1-123">Gibt den Namen des Integrations Kontopartners an.</span><span class="sxs-lookup"><span data-stu-id="8cdc1-123">Specifies the name of the integration account partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cdc1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cdc1-124">-ResourceGroupName</span></span>
<span data-ttu-id="8cdc1-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8cdc1-125">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cdc1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cdc1-126">CommonParameters</span></span>
<span data-ttu-id="8cdc1-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cdc1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cdc1-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cdc1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cdc1-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8cdc1-129">INPUTS</span></span>

### <span data-ttu-id="8cdc1-130">Keine</span><span class="sxs-lookup"><span data-stu-id="8cdc1-130">None</span></span>
<span data-ttu-id="8cdc1-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8cdc1-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8cdc1-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8cdc1-132">OUTPUTS</span></span>

### <span data-ttu-id="8cdc1-133">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="8cdc1-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="8cdc1-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="8cdc1-134">NOTES</span></span>

## <span data-ttu-id="8cdc1-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8cdc1-135">RELATED LINKS</span></span>

[<span data-ttu-id="8cdc1-136">Neu – AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="8cdc1-136">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="8cdc1-137">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="8cdc1-137">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="8cdc1-138">Satz-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="8cdc1-138">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


