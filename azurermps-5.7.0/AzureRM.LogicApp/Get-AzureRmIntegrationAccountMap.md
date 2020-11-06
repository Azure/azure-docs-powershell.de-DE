---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 340320ee102317069e81806ba9a7831dc1077368
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500558"
---
# <span data-ttu-id="44c35-101">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="44c35-101">Get-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="44c35-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="44c35-102">SYNOPSIS</span></span>
<span data-ttu-id="44c35-103">Ruft eine Integration-Kontozuordnung ab.</span><span class="sxs-lookup"><span data-stu-id="44c35-103">Gets an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44c35-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="44c35-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44c35-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44c35-105">DESCRIPTION</span></span>
<span data-ttu-id="44c35-106">Das Cmdlet " **Get-AzureRmIntegrationAccountMap** " Ruft die Integration-Kontozuordnung aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="44c35-106">The **Get-AzureRmIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="44c35-107">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Kartennamen an.</span><span class="sxs-lookup"><span data-stu-id="44c35-107">Specifying the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="44c35-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="44c35-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="44c35-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="44c35-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="44c35-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="44c35-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="44c35-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="44c35-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="44c35-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44c35-112">EXAMPLES</span></span>

### <span data-ttu-id="44c35-113">Beispiel 1: Abrufen einer Integrations Kontozuordnung</span><span class="sxs-lookup"><span data-stu-id="44c35-113">Example 1: Get an integration account map</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="44c35-114">Dieser Befehl ruft eine Integration-Kontozuordnung mit dem Namen IntegrationAccountMap47 in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="44c35-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="44c35-115">Beispiel 2: Abrufen von Integrations Kontozuordnungen nach dem Namen des Integrations Kontos</span><span class="sxs-lookup"><span data-stu-id="44c35-115">Example 2: Get integration account maps by integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="44c35-116">Mit diesem Befehl werden die Integrations Kontozuordnungen nach dem Namen des Integrations Kontos abgerufen.</span><span class="sxs-lookup"><span data-stu-id="44c35-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="44c35-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="44c35-117">PARAMETERS</span></span>

### <span data-ttu-id="44c35-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44c35-118">-DefaultProfile</span></span>
<span data-ttu-id="44c35-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="44c35-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44c35-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="44c35-120">-MapName</span></span>
<span data-ttu-id="44c35-121">Gibt den Namen einer Integrations Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="44c35-121">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="44c35-122">-Name</span><span class="sxs-lookup"><span data-stu-id="44c35-122">-Name</span></span>
<span data-ttu-id="44c35-123">Gibt den Namen für das Integrations Konto an.</span><span class="sxs-lookup"><span data-stu-id="44c35-123">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="44c35-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44c35-124">-ResourceGroupName</span></span>
<span data-ttu-id="44c35-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="44c35-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="44c35-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c35-126">CommonParameters</span></span>
<span data-ttu-id="44c35-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44c35-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c35-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44c35-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c35-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="44c35-129">INPUTS</span></span>

### <span data-ttu-id="44c35-130">Keine</span><span class="sxs-lookup"><span data-stu-id="44c35-130">None</span></span>
<span data-ttu-id="44c35-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="44c35-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="44c35-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="44c35-132">OUTPUTS</span></span>

### <span data-ttu-id="44c35-133">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="44c35-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="44c35-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="44c35-134">NOTES</span></span>

## <span data-ttu-id="44c35-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="44c35-135">RELATED LINKS</span></span>

[<span data-ttu-id="44c35-136">Neu – AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="44c35-136">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="44c35-137">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="44c35-137">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="44c35-138">Satz-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="44c35-138">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


