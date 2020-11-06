---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/stop-azurermlogicapprun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
ms.openlocfilehash: cd269c015870ab2a030ee44ebfd0f01874b674f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497398"
---
# <span data-ttu-id="ef7d1-101">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="ef7d1-101">Stop-AzureRmLogicAppRun</span></span>

## <span data-ttu-id="ef7d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef7d1-102">SYNOPSIS</span></span>
<span data-ttu-id="ef7d1-103">Bricht die Ausführung einer Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="ef7d1-103">Cancels a run of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef7d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef7d1-104">SYNTAX</span></span>

```
Stop-AzureRmLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef7d1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef7d1-105">DESCRIPTION</span></span>
<span data-ttu-id="ef7d1-106">Mit dem Cmdlet " **Stop-AzureRmLogicAppRun** " wird ein Testlauf einer Logik-App abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="ef7d1-106">The **Stop-AzureRmLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="ef7d1-107">Geben Sie die Logik-APP, die Ressourcengruppe und die Ausführung an.</span><span class="sxs-lookup"><span data-stu-id="ef7d1-107">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="ef7d1-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="ef7d1-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ef7d1-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="ef7d1-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ef7d1-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="ef7d1-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ef7d1-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="ef7d1-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ef7d1-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef7d1-112">EXAMPLES</span></span>

### <span data-ttu-id="ef7d1-113">Beispiel 1: Abbrechen einer Ausführung einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="ef7d1-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Stop-AzureRmLogicAppRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076" -Force
```

<span data-ttu-id="ef7d1-114">Mit diesem Befehl wird eine Ausführung der Logik-App mit dem Namen LogicApp03 abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="ef7d1-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="ef7d1-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef7d1-115">PARAMETERS</span></span>

### <span data-ttu-id="ef7d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef7d1-116">-DefaultProfile</span></span>
<span data-ttu-id="ef7d1-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ef7d1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef7d1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ef7d1-118">-Force</span></span>
<span data-ttu-id="ef7d1-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="ef7d1-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ef7d1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ef7d1-120">-Name</span></span>
<span data-ttu-id="ef7d1-121">Gibt den Namen einer Logik-APP an, für die dieses Cmdlet eine Ausführung abbricht.</span><span class="sxs-lookup"><span data-stu-id="ef7d1-121">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="ef7d1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef7d1-122">-ResourceGroupName</span></span>
<span data-ttu-id="ef7d1-123">Gibt den Namen für eine Ressourcengruppe an, in der mit diesem Cmdlet eine Ausführung abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="ef7d1-123">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

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

### <span data-ttu-id="ef7d1-124">-RunName</span><span class="sxs-lookup"><span data-stu-id="ef7d1-124">-RunName</span></span>
<span data-ttu-id="ef7d1-125">Gibt den Namen einer Logik-APP an, die vom Cmdlet abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="ef7d1-125">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

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

### <span data-ttu-id="ef7d1-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ef7d1-126">-Confirm</span></span>
<span data-ttu-id="ef7d1-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ef7d1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef7d1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef7d1-128">-WhatIf</span></span>
<span data-ttu-id="ef7d1-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef7d1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef7d1-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef7d1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef7d1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef7d1-131">CommonParameters</span></span>
<span data-ttu-id="ef7d1-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef7d1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef7d1-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef7d1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef7d1-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef7d1-134">INPUTS</span></span>

### <span data-ttu-id="ef7d1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ef7d1-135">System.String</span></span>

## <span data-ttu-id="ef7d1-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef7d1-136">OUTPUTS</span></span>

### <span data-ttu-id="ef7d1-137">System. void</span><span class="sxs-lookup"><span data-stu-id="ef7d1-137">System.Void</span></span>

## <span data-ttu-id="ef7d1-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef7d1-138">NOTES</span></span>

## <span data-ttu-id="ef7d1-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef7d1-139">RELATED LINKS</span></span>

[<span data-ttu-id="ef7d1-140">Anfang-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ef7d1-140">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


