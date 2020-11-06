---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 6f1f58f5f25b3e3ef4782bcc0ea8a4b3170eed81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479157"
---
# <span data-ttu-id="94c4d-101">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="94c4d-101">Get-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="94c4d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="94c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="94c4d-103">Ruft eine Integration-Kontozuordnung ab.</span><span class="sxs-lookup"><span data-stu-id="94c4d-103">Gets an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94c4d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="94c4d-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94c4d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94c4d-105">DESCRIPTION</span></span>
<span data-ttu-id="94c4d-106">Das Cmdlet " **Get-AzureRmIntegrationAccountMap** " Ruft die Integration-Kontozuordnung aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="94c4d-106">The **Get-AzureRmIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="94c4d-107">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Kartennamen an.</span><span class="sxs-lookup"><span data-stu-id="94c4d-107">Specifying the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="94c4d-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="94c4d-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="94c4d-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="94c4d-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="94c4d-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="94c4d-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="94c4d-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="94c4d-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="94c4d-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="94c4d-112">EXAMPLES</span></span>

### <span data-ttu-id="94c4d-113">Beispiel 1: Abrufen einer Integrations Kontozuordnung</span><span class="sxs-lookup"><span data-stu-id="94c4d-113">Example 1: Get an integration account map</span></span>
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

<span data-ttu-id="94c4d-114">Dieser Befehl ruft eine Integration-Kontozuordnung mit dem Namen IntegrationAccountMap47 in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="94c4d-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="94c4d-115">Beispiel 2: Abrufen von Integrations Kontozuordnungen nach dem Namen des Integrations Kontos</span><span class="sxs-lookup"><span data-stu-id="94c4d-115">Example 2: Get integration account maps by integration account name</span></span>
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

<span data-ttu-id="94c4d-116">Mit diesem Befehl werden die Integrations Kontozuordnungen nach dem Namen des Integrations Kontos abgerufen.</span><span class="sxs-lookup"><span data-stu-id="94c4d-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="94c4d-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="94c4d-117">PARAMETERS</span></span>

### <span data-ttu-id="94c4d-118">-MapName</span><span class="sxs-lookup"><span data-stu-id="94c4d-118">-MapName</span></span>
<span data-ttu-id="94c4d-119">Gibt den Namen einer Integrations Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="94c4d-119">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="94c4d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="94c4d-120">-Name</span></span>
<span data-ttu-id="94c4d-121">Gibt den Namen für das Integrations Konto an.</span><span class="sxs-lookup"><span data-stu-id="94c4d-121">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="94c4d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94c4d-122">-ResourceGroupName</span></span>
<span data-ttu-id="94c4d-123">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="94c4d-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="94c4d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c4d-124">-DefaultProfile</span></span>
<span data-ttu-id="94c4d-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="94c4d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c4d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c4d-126">CommonParameters</span></span>
<span data-ttu-id="94c4d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94c4d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c4d-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94c4d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c4d-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="94c4d-129">INPUTS</span></span>

## <span data-ttu-id="94c4d-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="94c4d-130">OUTPUTS</span></span>

### <span data-ttu-id="94c4d-131">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="94c4d-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="94c4d-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="94c4d-132">NOTES</span></span>

## <span data-ttu-id="94c4d-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="94c4d-133">RELATED LINKS</span></span>

[<span data-ttu-id="94c4d-134">Neu – AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="94c4d-134">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="94c4d-135">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="94c4d-135">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="94c4d-136">Satz-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="94c4d-136">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


