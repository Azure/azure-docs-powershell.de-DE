---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
ms.openlocfilehash: b13e7b63994f71f51f321428472169aea52e92f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472330"
---
# <span data-ttu-id="5cd78-101">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="5cd78-101">Get-AzIntegrationAccount</span></span>

## <span data-ttu-id="5cd78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cd78-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd78-103">Ruft Integrationskonten ab.</span><span class="sxs-lookup"><span data-stu-id="5cd78-103">Gets integration accounts.</span></span>

## <span data-ttu-id="5cd78-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5cd78-104">SYNTAX</span></span>

```
Get-AzIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cd78-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5cd78-105">DESCRIPTION</span></span>
<span data-ttu-id="5cd78-106">Das **Cmdlet "Get-AzIntegrationAccount"** ruft Integrationskonten aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="5cd78-106">The **Get-AzIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="5cd78-107">Geben Sie den Namen eines Integrationskontos und einen Ressourcengruppennamen an.</span><span class="sxs-lookup"><span data-stu-id="5cd78-107">Specify an integration account name and resource group name.</span></span>
<span data-ttu-id="5cd78-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="5cd78-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5cd78-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="5cd78-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5cd78-110">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="5cd78-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5cd78-111">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="5cd78-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5cd78-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5cd78-112">EXAMPLES</span></span>

### <span data-ttu-id="5cd78-113">Beispiel 1: Erhalten eines Integrationskontos nach Name</span><span class="sxs-lookup"><span data-stu-id="5cd78-113">Example 1: Get an integration account by name</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="5cd78-114">Dieser Befehl ruft ein Integrationskonto namens "IntegrationAccount31" aus der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="5cd78-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="5cd78-115">Beispiel 2: Erhalten von Integrationskonten in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5cd78-115">Example 2: Get integration accounts in a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="5cd78-116">Dieser Befehl ruft Integrationskonten aus einer Ressourcengruppe namens "ResourceGroup11" ab.</span><span class="sxs-lookup"><span data-stu-id="5cd78-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="5cd78-117">Beispiel 3: Alle Integrationskonten erhalten</span><span class="sxs-lookup"><span data-stu-id="5cd78-117">Example 3: Get all integration accounts</span></span>
```
PS C:\>Get-AzIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="5cd78-118">Dieser Befehl ruft alle Integrationskonten in Ihrem Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="5cd78-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="5cd78-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cd78-119">PARAMETERS</span></span>

### <span data-ttu-id="5cd78-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cd78-120">-DefaultProfile</span></span>
<span data-ttu-id="5cd78-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5cd78-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5cd78-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5cd78-122">-Name</span></span>
<span data-ttu-id="5cd78-123">Gibt den Namen eines Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="5cd78-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="5cd78-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cd78-124">-ResourceGroupName</span></span>
<span data-ttu-id="5cd78-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="5cd78-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5cd78-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd78-126">CommonParameters</span></span>
<span data-ttu-id="5cd78-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cd78-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd78-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cd78-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd78-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5cd78-129">INPUTS</span></span>

### <span data-ttu-id="5cd78-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5cd78-130">System.String</span></span>

## <span data-ttu-id="5cd78-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5cd78-131">OUTPUTS</span></span>

### <span data-ttu-id="5cd78-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="5cd78-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="5cd78-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5cd78-133">NOTES</span></span>

## <span data-ttu-id="5cd78-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5cd78-134">RELATED LINKS</span></span>

[<span data-ttu-id="5cd78-135">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="5cd78-135">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="5cd78-136">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="5cd78-136">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="5cd78-137">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="5cd78-137">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="5cd78-138">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="5cd78-138">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


