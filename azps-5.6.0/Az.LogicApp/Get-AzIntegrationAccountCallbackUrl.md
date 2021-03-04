---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
ms.openlocfilehash: c23e8ca566db3a3b3c93dcdc7a4fc53fc85979c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922928"
---
# <span data-ttu-id="25262-101">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="25262-101">Get-AzIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="25262-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25262-102">SYNOPSIS</span></span>
<span data-ttu-id="25262-103">Ruft eine Rückruf-URL für ein Integrationskonto ab.</span><span class="sxs-lookup"><span data-stu-id="25262-103">Gets an integration account callback URL.</span></span>

## <span data-ttu-id="25262-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25262-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25262-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25262-105">DESCRIPTION</span></span>
<span data-ttu-id="25262-106">Das **Get-AzIntegrationAccountCallbackUrl-Cmdlet** ruft eine Rückruf-URL für Integrationskonten aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="25262-106">The **Get-AzIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="25262-107">Dieses Cmdlet gibt ein **Rückrufobjekt** zurück, das die Rückruf-URL des Integrationskontos darstellt.</span><span class="sxs-lookup"><span data-stu-id="25262-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="25262-108">Geben Sie den Namen des Integrationskontos und den Ressourcengruppennamen an.</span><span class="sxs-lookup"><span data-stu-id="25262-108">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="25262-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="25262-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="25262-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="25262-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="25262-111">Um die Namen dynamischer Parameter zu ermitteln, geben Sie nach dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="25262-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="25262-112">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="25262-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="25262-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="25262-113">EXAMPLES</span></span>

### <span data-ttu-id="25262-114">Beispiel 1: Aufrufen einer Rückruf-URL für ein Integrationskonto</span><span class="sxs-lookup"><span data-stu-id="25262-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="25262-115">Dieser Befehl ruft eine Rückruf-URL des Integrationskontos ab.</span><span class="sxs-lookup"><span data-stu-id="25262-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="25262-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="25262-116">PARAMETERS</span></span>

### <span data-ttu-id="25262-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25262-117">-DefaultProfile</span></span>
<span data-ttu-id="25262-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="25262-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25262-119">-Name</span><span class="sxs-lookup"><span data-stu-id="25262-119">-Name</span></span>
<span data-ttu-id="25262-120">Gibt den Namen eines Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="25262-120">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="25262-121">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="25262-121">-NotAfter</span></span>
<span data-ttu-id="25262-122">Gibt das Ablaufdatum für die Rückruf-URL an.</span><span class="sxs-lookup"><span data-stu-id="25262-122">Specifies the expiry date for the callback URL.</span></span>

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

### <span data-ttu-id="25262-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25262-123">-ResourceGroupName</span></span>
<span data-ttu-id="25262-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="25262-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="25262-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25262-125">CommonParameters</span></span>
<span data-ttu-id="25262-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25262-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25262-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25262-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25262-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="25262-128">INPUTS</span></span>

### <span data-ttu-id="25262-129">System.String</span><span class="sxs-lookup"><span data-stu-id="25262-129">System.String</span></span>

## <span data-ttu-id="25262-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="25262-130">OUTPUTS</span></span>

### <span data-ttu-id="25262-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="25262-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="25262-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="25262-132">NOTES</span></span>

## <span data-ttu-id="25262-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="25262-133">RELATED LINKS</span></span>

[<span data-ttu-id="25262-134">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="25262-134">Get-AzLogicAppTriggerCallbackUrl</span></span>](./Get-AzLogicAppTriggerCallbackUrl.md)


