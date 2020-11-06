---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: 06aebcf21b7a9fb69887c8922343faf7867d796c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502074"
---
# <span data-ttu-id="2a021-101">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="2a021-101">Get-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="2a021-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2a021-102">SYNOPSIS</span></span>
<span data-ttu-id="2a021-103">Ruft Schemas für das Integrations Konto ab.</span><span class="sxs-lookup"><span data-stu-id="2a021-103">Gets integration account schemas.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a021-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a021-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a021-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a021-105">DESCRIPTION</span></span>
<span data-ttu-id="2a021-106">Das Cmdlet " **Get-AzureRmIntegrationAccountSchema** " ruft Schemas für das Integrations Konto ab.</span><span class="sxs-lookup"><span data-stu-id="2a021-106">The **Get-AzureRmIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="2a021-107">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Schemanamen an.</span><span class="sxs-lookup"><span data-stu-id="2a021-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="2a021-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="2a021-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="2a021-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="2a021-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="2a021-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="2a021-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2a021-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="2a021-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2a021-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2a021-112">EXAMPLES</span></span>

### <span data-ttu-id="2a021-113">Beispiel 1: Abrufen eines Schemas für ein Integrations Konto</span><span class="sxs-lookup"><span data-stu-id="2a021-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="2a021-114">Dieser Befehl ruft das Schema des Integrations Kontos mit dem Namen IntegrationAccountSchema43 ab.</span><span class="sxs-lookup"><span data-stu-id="2a021-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="2a021-115">Beispiel 2: Abrufen von Integrations Konto Schemas für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="2a021-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="2a021-116">Dieser Befehl ruft die Schemas für das Integrations Konto für die Ressourcengruppe mit dem Namen ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="2a021-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="2a021-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a021-117">PARAMETERS</span></span>

### <span data-ttu-id="2a021-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a021-118">-DefaultProfile</span></span>
<span data-ttu-id="2a021-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2a021-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a021-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2a021-120">-Name</span></span>
<span data-ttu-id="2a021-121">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="2a021-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="2a021-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a021-122">-ResourceGroupName</span></span>
<span data-ttu-id="2a021-123">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2a021-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2a021-124">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="2a021-124">-SchemaName</span></span>
<span data-ttu-id="2a021-125">Gibt den Namen eines Schemas für ein Integrations Konto an.</span><span class="sxs-lookup"><span data-stu-id="2a021-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="2a021-126">Gibt den Namen eines Schemas an.</span><span class="sxs-lookup"><span data-stu-id="2a021-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="2a021-127">.</span><span class="sxs-lookup"><span data-stu-id="2a021-127">.</span></span>

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

### <span data-ttu-id="2a021-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a021-128">CommonParameters</span></span>
<span data-ttu-id="2a021-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a021-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a021-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a021-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a021-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2a021-131">INPUTS</span></span>

### <span data-ttu-id="2a021-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2a021-132">System.String</span></span>

## <span data-ttu-id="2a021-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2a021-133">OUTPUTS</span></span>

### <span data-ttu-id="2a021-134">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="2a021-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="2a021-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="2a021-135">NOTES</span></span>

## <span data-ttu-id="2a021-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2a021-136">RELATED LINKS</span></span>

[<span data-ttu-id="2a021-137">Neu – AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="2a021-137">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="2a021-138">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="2a021-138">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="2a021-139">Satz-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="2a021-139">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


