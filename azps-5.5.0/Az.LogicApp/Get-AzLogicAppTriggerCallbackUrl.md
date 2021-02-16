---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggercallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: 8f45141fc937710a5369ebfac208705ca1ee3ba3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157553"
---
# <span data-ttu-id="a92c1-101">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="a92c1-101">Get-AzLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="a92c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a92c1-102">SYNOPSIS</span></span>
<span data-ttu-id="a92c1-103">Ruft eine Rückruf-URL für den Trigger der Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="a92c1-103">Gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="a92c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a92c1-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a92c1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a92c1-105">DESCRIPTION</span></span>
<span data-ttu-id="a92c1-106">Das **Cmdlet "Get-AzLogicAppTriggerCallbackUrl"** ruft eine Rückruf-URL für die Logik-App-Trigger aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="a92c1-106">The **Get-AzLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="a92c1-107">Dieses Cmdlet gibt ein **WorkflowTriggerCallbackUrl-Objekt** zurück, das die Rückruf-URL darstellt.</span><span class="sxs-lookup"><span data-stu-id="a92c1-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="a92c1-108">Geben Sie den Namen der Ressourcengruppe, den Namen der Logik-App und den Triggernamen an.</span><span class="sxs-lookup"><span data-stu-id="a92c1-108">Specify the resource group name, logic app name, and trigger name.</span></span>
<span data-ttu-id="a92c1-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="a92c1-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a92c1-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="a92c1-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a92c1-111">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="a92c1-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a92c1-112">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="a92c1-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a92c1-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a92c1-113">EXAMPLES</span></span>

### <span data-ttu-id="a92c1-114">Beispiel 1: Rufen Sie die Rückruf-URL für den Trigger einer Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="a92c1-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="a92c1-115">Dieser Befehl ruft eine Rückruf-URL für den Trigger der Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="a92c1-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="a92c1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a92c1-116">PARAMETERS</span></span>

### <span data-ttu-id="a92c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a92c1-117">-DefaultProfile</span></span>
<span data-ttu-id="a92c1-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a92c1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a92c1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a92c1-119">-Name</span></span>
<span data-ttu-id="a92c1-120">Gibt den Namen einer Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="a92c1-120">Specifies the name of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a92c1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a92c1-121">-ResourceGroupName</span></span>
<span data-ttu-id="a92c1-122">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a92c1-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a92c1-123">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="a92c1-123">-TriggerName</span></span>
<span data-ttu-id="a92c1-124">Gibt den Namen eines Triggers an.</span><span class="sxs-lookup"><span data-stu-id="a92c1-124">Specifies the name of a trigger.</span></span>

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

### <span data-ttu-id="a92c1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a92c1-125">CommonParameters</span></span>
<span data-ttu-id="a92c1-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a92c1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a92c1-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a92c1-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a92c1-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a92c1-128">INPUTS</span></span>

### <span data-ttu-id="a92c1-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a92c1-129">System.String</span></span>

## <span data-ttu-id="a92c1-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a92c1-130">OUTPUTS</span></span>

### <span data-ttu-id="a92c1-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="a92c1-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="a92c1-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a92c1-132">NOTES</span></span>

## <span data-ttu-id="a92c1-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a92c1-133">RELATED LINKS</span></span>

[<span data-ttu-id="a92c1-134">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="a92c1-134">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)


