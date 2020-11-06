---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptriggercallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: 7c7dcac142beb809b95c573d89ef0a912fd1d0b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479770"
---
# <span data-ttu-id="c5348-101">Get-AzureRmLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="c5348-101">Get-AzureRmLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="c5348-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5348-102">SYNOPSIS</span></span>
<span data-ttu-id="c5348-103">Ruft eine Logik-App-Trigger-Rückruf-URL ab.</span><span class="sxs-lookup"><span data-stu-id="c5348-103">Gets a Logic App trigger callback URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5348-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5348-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5348-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5348-105">DESCRIPTION</span></span>
<span data-ttu-id="c5348-106">Das Cmdlet " **Get-AzureRmLogicAppTriggerCallbackUrl** " Ruft eine Logik-App zum Auslösen einer Rückruf-URL aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="c5348-106">The **Get-AzureRmLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="c5348-107">Dieses Cmdlet gibt ein **WorkflowTriggerCallbackUrl** -Objekt zurück, das die Rückruf-URL darstellt.</span><span class="sxs-lookup"><span data-stu-id="c5348-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="c5348-108">Geben Sie den Namen der Ressourcengruppe, den Logik-APP-Namen und den Triggernamen an.</span><span class="sxs-lookup"><span data-stu-id="c5348-108">Specify the resource group name, logic app name, and trigger name.</span></span>

<span data-ttu-id="c5348-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="c5348-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c5348-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="c5348-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c5348-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="c5348-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c5348-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="c5348-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c5348-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5348-113">EXAMPLES</span></span>

### <span data-ttu-id="c5348-114">Beispiel 1: Abrufen einer Logic App-Trigger-Rückruf-URL</span><span class="sxs-lookup"><span data-stu-id="c5348-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="c5348-115">Dieser Befehl ruft eine Logik-App-Rückruf-URL ab.</span><span class="sxs-lookup"><span data-stu-id="c5348-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="c5348-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5348-116">PARAMETERS</span></span>

### <span data-ttu-id="c5348-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5348-117">-DefaultProfile</span></span>
<span data-ttu-id="c5348-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c5348-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5348-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c5348-119">-Name</span></span>
<span data-ttu-id="c5348-120">Gibt den Namen einer Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="c5348-120">Specifies the name of a logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5348-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5348-121">-ResourceGroupName</span></span>
<span data-ttu-id="c5348-122">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c5348-122">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5348-123">-Triggername</span><span class="sxs-lookup"><span data-stu-id="c5348-123">-TriggerName</span></span>
<span data-ttu-id="c5348-124">Gibt den Namen eines Triggers an.</span><span class="sxs-lookup"><span data-stu-id="c5348-124">Specifies the name of a trigger.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5348-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5348-125">CommonParameters</span></span>
<span data-ttu-id="c5348-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5348-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5348-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5348-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5348-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5348-128">INPUTS</span></span>

### <span data-ttu-id="c5348-129">Keine</span><span class="sxs-lookup"><span data-stu-id="c5348-129">None</span></span>
<span data-ttu-id="c5348-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c5348-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c5348-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5348-131">OUTPUTS</span></span>

### <span data-ttu-id="c5348-132">Microsoft. Azure. Management. Logic. Models. WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="c5348-132">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="c5348-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5348-133">NOTES</span></span>

## <span data-ttu-id="c5348-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5348-134">RELATED LINKS</span></span>

[<span data-ttu-id="c5348-135">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="c5348-135">Get-AzureRmIntegrationAccountCallbackUrl</span></span>](./Get-AzureRmIntegrationAccountCallbackUrl.md)


