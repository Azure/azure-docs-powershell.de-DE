---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: 2d9425f21845123c003568204675b0d56a8bcd02
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845968"
---
# <span data-ttu-id="0c9fd-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="0c9fd-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="0c9fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c9fd-102">SYNOPSIS</span></span>
<span data-ttu-id="0c9fd-103">Ruft den Ausführungsverlauf einer Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="0c9fd-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="0c9fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c9fd-104">SYNTAX</span></span>

```
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c9fd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c9fd-105">DESCRIPTION</span></span>
<span data-ttu-id="0c9fd-106">Das Cmdlet " **Get-AzLogicAppRunHistory** " Ruft den Ausführungsverlauf einer Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="0c9fd-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="0c9fd-107">Dieses Cmdlet gibt eine Sammlung von **WorkflowRun** -Objekten zurück.</span><span class="sxs-lookup"><span data-stu-id="0c9fd-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="0c9fd-108">Geben Sie die Logik-APP und die Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0c9fd-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="0c9fd-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="0c9fd-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0c9fd-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="0c9fd-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0c9fd-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="0c9fd-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0c9fd-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="0c9fd-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0c9fd-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c9fd-113">EXAMPLES</span></span>

### <span data-ttu-id="0c9fd-114">Beispiel 1: Abrufen des Ausführungsverlaufs einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="0c9fd-114">Example 1: Get the run history of a logic app</span></span>
```
PS C:\>Get-AzLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952540

CorrelationId    : d3ddc917-9aaa-47b3-8814-c621c2ae530b
EndTime          : 1/13/2016 2:42:56 PM
Error            : {code, message}
Name             : 08587489107100664541
Outputs          : {}
StartTime        : 1/13/2016 2:42:55 PM
Status           : Failed
TriggerName      : httpTrigger
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="0c9fd-115">Dieser Befehl ruft den Ausführungsverlauf einer Logik-App mit dem Namen LogicApp03 ab.</span><span class="sxs-lookup"><span data-stu-id="0c9fd-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="0c9fd-116">Beispiel 2: Abrufen einer Logik-App-Ausführung</span><span class="sxs-lookup"><span data-stu-id="0c9fd-116">Example 2: Get a logic app run</span></span>
```
PS C:\>Get-AzLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="0c9fd-117">Dieser Befehl ruft eine bestimmte Logik-App für die Logik-App mit dem Namen LogicApp03 ab.</span><span class="sxs-lookup"><span data-stu-id="0c9fd-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

## <span data-ttu-id="0c9fd-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c9fd-118">PARAMETERS</span></span>

### <span data-ttu-id="0c9fd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c9fd-119">-DefaultProfile</span></span>
<span data-ttu-id="0c9fd-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0c9fd-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c9fd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0c9fd-121">-Name</span></span>
<span data-ttu-id="0c9fd-122">Gibt den Namen der Logik-APP an, für die dieses Cmdlet den Ausführungsverlauf erhält.</span><span class="sxs-lookup"><span data-stu-id="0c9fd-122">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c9fd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c9fd-123">-ResourceGroupName</span></span>
<span data-ttu-id="0c9fd-124">Gibt den Namen einer Ressourcengruppe an, die die Logik-app enthält.</span><span class="sxs-lookup"><span data-stu-id="0c9fd-124">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="0c9fd-125">-RunName</span><span class="sxs-lookup"><span data-stu-id="0c9fd-125">-RunName</span></span>
<span data-ttu-id="0c9fd-126">Gibt den Ausführungs Namen einer Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="0c9fd-126">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="0c9fd-127">Mit diesem Cmdlet wird der von diesem Cmdlet festgelegte Workflow ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c9fd-127">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="0c9fd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c9fd-128">CommonParameters</span></span>
<span data-ttu-id="0c9fd-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c9fd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c9fd-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c9fd-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c9fd-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c9fd-131">INPUTS</span></span>

### <span data-ttu-id="0c9fd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0c9fd-132">System.String</span></span>

## <span data-ttu-id="0c9fd-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c9fd-133">OUTPUTS</span></span>

### <span data-ttu-id="0c9fd-134">Microsoft. Azure. Management. Logic. Models. WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="0c9fd-134">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="0c9fd-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c9fd-135">NOTES</span></span>

## <span data-ttu-id="0c9fd-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c9fd-136">RELATED LINKS</span></span>

[<span data-ttu-id="0c9fd-137">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="0c9fd-137">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="0c9fd-138">Anfang-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="0c9fd-138">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="0c9fd-139">Stopp-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="0c9fd-139">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


