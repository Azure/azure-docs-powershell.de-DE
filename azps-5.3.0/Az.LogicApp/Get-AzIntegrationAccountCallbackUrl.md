---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 91a61935552258e5ca52ded6e05729deecaf5665
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472328"
---
# <span data-ttu-id="975df-101">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="975df-101">Get-AzIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="975df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="975df-102">SYNOPSIS</span></span>
<span data-ttu-id="975df-103">Ruft die Rückruf-URL für das Integrationskonto ab.</span><span class="sxs-lookup"><span data-stu-id="975df-103">Gets an integration account callback URL.</span></span>

## <span data-ttu-id="975df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="975df-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="975df-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="975df-105">DESCRIPTION</span></span>
<span data-ttu-id="975df-106">Das **Cmdlet "Get-AzIntegrationAccountCallbackUrl"** ruft eine Rückruf-URL für das Integrationskonto aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="975df-106">The **Get-AzIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="975df-107">Dieses Cmdlet gibt ein **CallbackUrl-Objekt** zurück, das die Rückruf-URL des Integrationskontos darstellt.</span><span class="sxs-lookup"><span data-stu-id="975df-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="975df-108">Geben Sie den Namen des Integrationskontos und den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="975df-108">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="975df-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="975df-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="975df-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="975df-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="975df-111">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="975df-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="975df-112">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="975df-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="975df-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="975df-113">EXAMPLES</span></span>

### <span data-ttu-id="975df-114">Beispiel 1: Aufrufen der Rückruf-URL für ein Integrationskonto</span><span class="sxs-lookup"><span data-stu-id="975df-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="975df-115">Dieser Befehl ruft eine Rückruf-URL für das Integrationskonto ab.</span><span class="sxs-lookup"><span data-stu-id="975df-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="975df-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="975df-116">PARAMETERS</span></span>

### <span data-ttu-id="975df-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="975df-117">-DefaultProfile</span></span>
<span data-ttu-id="975df-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="975df-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="975df-119">-Name</span><span class="sxs-lookup"><span data-stu-id="975df-119">-Name</span></span>
<span data-ttu-id="975df-120">Gibt den Namen eines Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="975df-120">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="975df-121">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="975df-121">-NotAfter</span></span>
<span data-ttu-id="975df-122">Gibt das Ablaufdatum für die Rückruf-URL an.</span><span class="sxs-lookup"><span data-stu-id="975df-122">Specifies the expiry date for the callback URL.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="975df-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="975df-123">-ResourceGroupName</span></span>
<span data-ttu-id="975df-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="975df-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="975df-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="975df-125">CommonParameters</span></span>
<span data-ttu-id="975df-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="975df-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="975df-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="975df-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="975df-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="975df-128">INPUTS</span></span>

### <span data-ttu-id="975df-129">System.String</span><span class="sxs-lookup"><span data-stu-id="975df-129">System.String</span></span>

## <span data-ttu-id="975df-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="975df-130">OUTPUTS</span></span>

### <span data-ttu-id="975df-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="975df-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="975df-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="975df-132">NOTES</span></span>

## <span data-ttu-id="975df-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="975df-133">RELATED LINKS</span></span>

[<span data-ttu-id="975df-134">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="975df-134">Get-AzLogicAppTriggerCallbackUrl</span></span>](./Get-AzLogicAppTriggerCallbackUrl.md)


