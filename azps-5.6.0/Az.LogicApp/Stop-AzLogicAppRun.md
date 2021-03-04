---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: https://docs.microsoft.com/powershell/module/az.logicapp/stop-azlogicapprun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
ms.openlocfilehash: 975e819e4b52e1fa09bd8068b630f540e34e72bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918827"
---
# <span data-ttu-id="dfb26-101">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="dfb26-101">Stop-AzLogicAppRun</span></span>

## <span data-ttu-id="dfb26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfb26-102">SYNOPSIS</span></span>
<span data-ttu-id="dfb26-103">Bricht die Ausführung einer Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="dfb26-103">Cancels a run of a logic app.</span></span>

## <span data-ttu-id="dfb26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfb26-104">SYNTAX</span></span>

```
Stop-AzLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfb26-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dfb26-105">DESCRIPTION</span></span>
<span data-ttu-id="dfb26-106">Das **Cmdlet Stop-AzLogicAppRun** beendet die Ausführung einer Logik-App.</span><span class="sxs-lookup"><span data-stu-id="dfb26-106">The **Stop-AzLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="dfb26-107">Geben Sie die Logik-App, die Ressourcengruppe und die Ausführung an.</span><span class="sxs-lookup"><span data-stu-id="dfb26-107">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="dfb26-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="dfb26-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="dfb26-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="dfb26-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="dfb26-110">Um die Namen dynamischer Parameter zu ermitteln, geben Sie nach dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="dfb26-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="dfb26-111">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="dfb26-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="dfb26-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dfb26-112">EXAMPLES</span></span>

### <span data-ttu-id="dfb26-113">Beispiel 1: Abbrechen einer Ausführung einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="dfb26-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Stop-AzLogicAppRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076" -Force
```

<span data-ttu-id="dfb26-114">Mit diesem Befehl wird die Ausführung der Logik-App mit dem Namen LogicApp03 abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="dfb26-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="dfb26-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dfb26-115">PARAMETERS</span></span>

### <span data-ttu-id="dfb26-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfb26-116">-DefaultProfile</span></span>
<span data-ttu-id="dfb26-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="dfb26-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfb26-118">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="dfb26-118">-Force</span></span>
<span data-ttu-id="dfb26-119">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="dfb26-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfb26-120">-Name</span><span class="sxs-lookup"><span data-stu-id="dfb26-120">-Name</span></span>
<span data-ttu-id="dfb26-121">Gibt den Namen einer Logik-App an, für die dieses Cmdlet eine Ausführung abbricht.</span><span class="sxs-lookup"><span data-stu-id="dfb26-121">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="dfb26-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfb26-122">-ResourceGroupName</span></span>
<span data-ttu-id="dfb26-123">Gibt den Namen für eine Ressourcengruppe an, in der dieses Cmdlet eine Ausführung abbricht.</span><span class="sxs-lookup"><span data-stu-id="dfb26-123">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="dfb26-124">-RunName</span><span class="sxs-lookup"><span data-stu-id="dfb26-124">-RunName</span></span>
<span data-ttu-id="dfb26-125">Gibt den Namen einer Logik-App an, die von diesem Cmdlet abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="dfb26-125">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="dfb26-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dfb26-126">-Confirm</span></span>
<span data-ttu-id="dfb26-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dfb26-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfb26-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfb26-128">-WhatIf</span></span>
<span data-ttu-id="dfb26-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dfb26-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfb26-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dfb26-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfb26-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfb26-131">CommonParameters</span></span>
<span data-ttu-id="dfb26-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfb26-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfb26-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfb26-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfb26-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dfb26-134">INPUTS</span></span>

### <span data-ttu-id="dfb26-135">System.String</span><span class="sxs-lookup"><span data-stu-id="dfb26-135">System.String</span></span>

## <span data-ttu-id="dfb26-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dfb26-136">OUTPUTS</span></span>

### <span data-ttu-id="dfb26-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="dfb26-137">System.Void</span></span>

## <span data-ttu-id="dfb26-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dfb26-138">NOTES</span></span>

## <span data-ttu-id="dfb26-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dfb26-139">RELATED LINKS</span></span>

[<span data-ttu-id="dfb26-140">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="dfb26-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


