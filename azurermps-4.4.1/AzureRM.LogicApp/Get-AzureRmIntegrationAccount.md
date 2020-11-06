---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
ms.openlocfilehash: 441681cd33fe7715fbbb6fb244848c287f14ebb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479174"
---
# <span data-ttu-id="18dd0-101">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="18dd0-101">Get-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="18dd0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="18dd0-102">SYNOPSIS</span></span>
<span data-ttu-id="18dd0-103">Ruft Integrations Konten ab.</span><span class="sxs-lookup"><span data-stu-id="18dd0-103">Gets integration accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18dd0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="18dd0-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18dd0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18dd0-105">DESCRIPTION</span></span>
<span data-ttu-id="18dd0-106">Das Cmdlet " **Get-AzureRmIntegrationAccount** " ruft Integrations Konten aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="18dd0-106">The **Get-AzureRmIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="18dd0-107">Geben Sie einen Namen für den Integrations Kontonamen und die Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="18dd0-107">Specify an integration account name and resource group name.</span></span>

<span data-ttu-id="18dd0-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="18dd0-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="18dd0-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="18dd0-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="18dd0-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="18dd0-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="18dd0-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="18dd0-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="18dd0-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18dd0-112">EXAMPLES</span></span>

### <span data-ttu-id="18dd0-113">Beispiel 1: Abrufen eines Integrations Kontos nach Name</span><span class="sxs-lookup"><span data-stu-id="18dd0-113">Example 1: Get an integration account by name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="18dd0-114">Dieser Befehl ruft ein Integrations Konto mit dem Namen IntegrationAccount31 aus der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="18dd0-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="18dd0-115">Beispiel 2: Abrufen von Integrations Konten in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="18dd0-115">Example 2: Get integration accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="18dd0-116">Dieser Befehl ruft Integrations Konten aus einer Ressourcengruppe mit dem Namen ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="18dd0-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="18dd0-117">Beispiel 3: Abrufen aller Integrations Konten</span><span class="sxs-lookup"><span data-stu-id="18dd0-117">Example 3: Get all integration accounts</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="18dd0-118">Dieser Befehl ruft alle Integrations Konten in Ihrem Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="18dd0-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="18dd0-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="18dd0-119">PARAMETERS</span></span>

### <span data-ttu-id="18dd0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="18dd0-120">-Name</span></span>
<span data-ttu-id="18dd0-121">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="18dd0-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="18dd0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18dd0-122">-ResourceGroupName</span></span>
<span data-ttu-id="18dd0-123">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="18dd0-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="18dd0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18dd0-124">-DefaultProfile</span></span>
<span data-ttu-id="18dd0-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="18dd0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18dd0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18dd0-126">CommonParameters</span></span>
<span data-ttu-id="18dd0-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18dd0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18dd0-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18dd0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18dd0-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="18dd0-129">INPUTS</span></span>

## <span data-ttu-id="18dd0-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="18dd0-130">OUTPUTS</span></span>

### <span data-ttu-id="18dd0-131">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="18dd0-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="18dd0-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="18dd0-132">NOTES</span></span>

## <span data-ttu-id="18dd0-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="18dd0-133">RELATED LINKS</span></span>

[<span data-ttu-id="18dd0-134">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="18dd0-134">Get-AzureRmIntegrationAccountCallbackUrl</span></span>](./Get-AzureRmIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="18dd0-135">Neu – AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="18dd0-135">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="18dd0-136">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="18dd0-136">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="18dd0-137">Satz-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="18dd0-137">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


