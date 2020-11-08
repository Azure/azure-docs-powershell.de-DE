---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: de1c40dc7c9f8fefb1a275394b066e8af96de211
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177916"
---
# <span data-ttu-id="8d192-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="8d192-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="8d192-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8d192-102">SYNOPSIS</span></span>
<span data-ttu-id="8d192-103">Ruft den Ausführungsverlauf einer Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="8d192-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="8d192-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d192-104">SYNTAX</span></span>

```
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d192-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d192-105">DESCRIPTION</span></span>
<span data-ttu-id="8d192-106">Das Cmdlet " **Get-AzLogicAppRunHistory** " Ruft den Ausführungsverlauf einer Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="8d192-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="8d192-107">Dieses Cmdlet gibt eine Sammlung von **WorkflowRun** -Objekten zurück.</span><span class="sxs-lookup"><span data-stu-id="8d192-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="8d192-108">Geben Sie die Logik-APP und die Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8d192-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="8d192-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="8d192-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8d192-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="8d192-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8d192-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="8d192-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8d192-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="8d192-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8d192-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d192-113">EXAMPLES</span></span>

### <span data-ttu-id="8d192-114">Beispiel 1: Abrufen des Ausführungsverlaufs einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="8d192-114">Example 1: Get the run history of a logic app</span></span>
```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
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

<span data-ttu-id="8d192-115">Dieser Befehl ruft den Ausführungsverlauf einer Logik-App mit dem Namen LogicApp03 ab.</span><span class="sxs-lookup"><span data-stu-id="8d192-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="8d192-116">Beispiel 2: Abrufen einer Logik-App-Ausführung</span><span class="sxs-lookup"><span data-stu-id="8d192-116">Example 2: Get a logic app run</span></span>
```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
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

<span data-ttu-id="8d192-117">Dieser Befehl ruft eine bestimmte Logik-App für die Logik-App mit dem Namen LogicApp03 ab.</span><span class="sxs-lookup"><span data-stu-id="8d192-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="8d192-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="8d192-118">Example 3</span></span>

<span data-ttu-id="8d192-119">Dieser Befehl ruft den Ausführungsverlauf einer Logik-App mit dem Namen LogicApp03 ab.</span><span class="sxs-lookup"><span data-stu-id="8d192-119">This command gets the run history of a logic app named LogicApp03.</span></span> <span data-ttu-id="8d192-120">automatisch</span><span class="sxs-lookup"><span data-stu-id="8d192-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzLogicAppRunHistory -Name 'IntegrationAccount31' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="8d192-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d192-121">PARAMETERS</span></span>

### <span data-ttu-id="8d192-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d192-122">-DefaultProfile</span></span>
<span data-ttu-id="8d192-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8d192-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d192-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8d192-124">-Name</span></span>
<span data-ttu-id="8d192-125">Gibt den Namen der Logik-APP an, für die dieses Cmdlet den Ausführungsverlauf erhält.</span><span class="sxs-lookup"><span data-stu-id="8d192-125">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

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

### <span data-ttu-id="8d192-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d192-126">-ResourceGroupName</span></span>
<span data-ttu-id="8d192-127">Gibt den Namen einer Ressourcengruppe an, die die Logik-app enthält.</span><span class="sxs-lookup"><span data-stu-id="8d192-127">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="8d192-128">-RunName</span><span class="sxs-lookup"><span data-stu-id="8d192-128">-RunName</span></span>
<span data-ttu-id="8d192-129">Gibt den Ausführungs Namen einer Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="8d192-129">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="8d192-130">Mit diesem Cmdlet wird der von diesem Cmdlet festgelegte Workflow ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d192-130">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="8d192-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d192-131">CommonParameters</span></span>
<span data-ttu-id="8d192-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d192-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d192-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d192-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d192-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8d192-134">INPUTS</span></span>

### <span data-ttu-id="8d192-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8d192-135">System.String</span></span>

## <span data-ttu-id="8d192-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8d192-136">OUTPUTS</span></span>

### <span data-ttu-id="8d192-137">Microsoft. Azure. Management. Logic. Models. WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="8d192-137">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="8d192-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="8d192-138">NOTES</span></span>

## <span data-ttu-id="8d192-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8d192-139">RELATED LINKS</span></span>

[<span data-ttu-id="8d192-140">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="8d192-140">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="8d192-141">Anfang-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8d192-141">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="8d192-142">Stopp-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="8d192-142">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


