---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
ms.openlocfilehash: ed85c1fea8bd338b3dd4f2a9e82ee5aac3f3b52b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369366"
---
# <span data-ttu-id="ddf9c-101">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="ddf9c-101">Get-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="ddf9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddf9c-102">SYNOPSIS</span></span>
<span data-ttu-id="ddf9c-103">Ruft Schemas für Integrationskonto ab.</span><span class="sxs-lookup"><span data-stu-id="ddf9c-103">Gets integration account schemas.</span></span>

## <span data-ttu-id="ddf9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ddf9c-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddf9c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddf9c-105">DESCRIPTION</span></span>
<span data-ttu-id="ddf9c-106">Das **Cmdlet "Get-AzIntegrationAccountSchema"** ruft Schemas für Integrationskonten ab.</span><span class="sxs-lookup"><span data-stu-id="ddf9c-106">The **Get-AzIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="ddf9c-107">Angeben des Namens des Integrationskontos, des Ressourcengruppennamens und des Schemanamens</span><span class="sxs-lookup"><span data-stu-id="ddf9c-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="ddf9c-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="ddf9c-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ddf9c-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="ddf9c-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ddf9c-110">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="ddf9c-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ddf9c-111">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="ddf9c-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ddf9c-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ddf9c-112">EXAMPLES</span></span>

### <span data-ttu-id="ddf9c-113">Beispiel 1: Erhalten eines Integrationskontoschemas</span><span class="sxs-lookup"><span data-stu-id="ddf9c-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
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

<span data-ttu-id="ddf9c-114">Dieser Befehl ruft das Integrationskontoschema namens "IntegrationAccountSchema43" ab.</span><span class="sxs-lookup"><span data-stu-id="ddf9c-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="ddf9c-115">Beispiel 2: Erhalten von Schemas für Integrationskonto für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ddf9c-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="ddf9c-116">Dieser Befehl ruft die Schemas für das Integrationskonto für die Ressourcengruppe mit dem Namen "ResourceGroup11" ab.</span><span class="sxs-lookup"><span data-stu-id="ddf9c-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="ddf9c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddf9c-117">PARAMETERS</span></span>

### <span data-ttu-id="ddf9c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddf9c-118">-DefaultProfile</span></span>
<span data-ttu-id="ddf9c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ddf9c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddf9c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ddf9c-120">-Name</span></span>
<span data-ttu-id="ddf9c-121">Gibt den Namen eines Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="ddf9c-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="ddf9c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddf9c-122">-ResourceGroupName</span></span>
<span data-ttu-id="ddf9c-123">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ddf9c-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ddf9c-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="ddf9c-124">-SchemaName</span></span>
<span data-ttu-id="ddf9c-125">Gibt den Namen eines Integrationskontoschemas an.</span><span class="sxs-lookup"><span data-stu-id="ddf9c-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="ddf9c-126">Gibt den Namen eines Schemas an.</span><span class="sxs-lookup"><span data-stu-id="ddf9c-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="ddf9c-127">.</span><span class="sxs-lookup"><span data-stu-id="ddf9c-127">.</span></span>

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

### <span data-ttu-id="ddf9c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddf9c-128">CommonParameters</span></span>
<span data-ttu-id="ddf9c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddf9c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddf9c-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddf9c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddf9c-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ddf9c-131">INPUTS</span></span>

### <span data-ttu-id="ddf9c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ddf9c-132">System.String</span></span>

## <span data-ttu-id="ddf9c-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ddf9c-133">OUTPUTS</span></span>

### <span data-ttu-id="ddf9c-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="ddf9c-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="ddf9c-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ddf9c-135">NOTES</span></span>

## <span data-ttu-id="ddf9c-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ddf9c-136">RELATED LINKS</span></span>

[<span data-ttu-id="ddf9c-137">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="ddf9c-137">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="ddf9c-138">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="ddf9c-138">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="ddf9c-139">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="ddf9c-139">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


