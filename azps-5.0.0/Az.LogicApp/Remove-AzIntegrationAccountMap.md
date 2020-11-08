---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
ms.openlocfilehash: 37e6fcbaf1347d9aec48f680de749bf0b967551a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179169"
---
# <span data-ttu-id="e57f8-101">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="e57f8-101">Remove-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="e57f8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e57f8-102">SYNOPSIS</span></span>
<span data-ttu-id="e57f8-103">Entfernt eine Integration-Kontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="e57f8-103">Removes an integration account map.</span></span>

## <span data-ttu-id="e57f8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e57f8-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e57f8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e57f8-105">DESCRIPTION</span></span>
<span data-ttu-id="e57f8-106">Das Cmdlet **Remove-AzIntegrationAccountMap** entfernt eine Integration-Kontozuordnung aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e57f8-106">The **Remove-AzIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="e57f8-107">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Kartennamen an.</span><span class="sxs-lookup"><span data-stu-id="e57f8-107">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="e57f8-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="e57f8-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e57f8-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="e57f8-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e57f8-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="e57f8-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e57f8-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="e57f8-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e57f8-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e57f8-112">EXAMPLES</span></span>

### <span data-ttu-id="e57f8-113">Beispiel 1: Entfernen einer Integration-Kontozuordnung</span><span class="sxs-lookup"><span data-stu-id="e57f8-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="e57f8-114">Dieser Befehl entfernt die Integrations Kontozuordnung mit dem Namen IntegrationAccountMap47.</span><span class="sxs-lookup"><span data-stu-id="e57f8-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="e57f8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e57f8-115">PARAMETERS</span></span>

### <span data-ttu-id="e57f8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e57f8-116">-DefaultProfile</span></span>
<span data-ttu-id="e57f8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e57f8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e57f8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e57f8-118">-Force</span></span>
<span data-ttu-id="e57f8-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="e57f8-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e57f8-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="e57f8-120">-MapName</span></span>
<span data-ttu-id="e57f8-121">Gibt den Namen der Integrations Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="e57f8-121">Specifies the name of the integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e57f8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e57f8-122">-Name</span></span>
<span data-ttu-id="e57f8-123">Gibt den Namen des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="e57f8-123">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e57f8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e57f8-124">-ResourceGroupName</span></span>
<span data-ttu-id="e57f8-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e57f8-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e57f8-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e57f8-126">-Confirm</span></span>
<span data-ttu-id="e57f8-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e57f8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e57f8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e57f8-128">-WhatIf</span></span>
<span data-ttu-id="e57f8-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e57f8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e57f8-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e57f8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e57f8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e57f8-131">CommonParameters</span></span>
<span data-ttu-id="e57f8-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e57f8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e57f8-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e57f8-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e57f8-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e57f8-134">INPUTS</span></span>

### <span data-ttu-id="e57f8-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e57f8-135">System.String</span></span>

## <span data-ttu-id="e57f8-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e57f8-136">OUTPUTS</span></span>

### <span data-ttu-id="e57f8-137">System. void</span><span class="sxs-lookup"><span data-stu-id="e57f8-137">System.Void</span></span>

## <span data-ttu-id="e57f8-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="e57f8-138">NOTES</span></span>

## <span data-ttu-id="e57f8-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e57f8-139">RELATED LINKS</span></span>

[<span data-ttu-id="e57f8-140">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="e57f8-140">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="e57f8-141">Neu – AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="e57f8-141">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="e57f8-142">Satz-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="e57f8-142">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


