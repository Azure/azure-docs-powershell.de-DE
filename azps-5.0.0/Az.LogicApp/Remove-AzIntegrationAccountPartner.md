---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
ms.openlocfilehash: ee4f24356c33aac0940a10905b52199bd06d2a47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179165"
---
# <span data-ttu-id="e0f1f-101">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="e0f1f-101">Remove-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="e0f1f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e0f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f1f-103">Entfernt einen Integrations Kontopartner.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-103">Removes an integration account partner.</span></span>

## <span data-ttu-id="e0f1f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0f1f-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0f1f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0f1f-105">DESCRIPTION</span></span>
<span data-ttu-id="e0f1f-106">Das Cmdlet **Remove-AzIntegrationAccountPartner** entfernt einen Integrations Kontopartner aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-106">The **Remove-AzIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="e0f1f-107">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Partnernamen an.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="e0f1f-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e0f1f-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e0f1f-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e0f1f-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e0f1f-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0f1f-112">EXAMPLES</span></span>

### <span data-ttu-id="e0f1f-113">Beispiel 1: Entfernen eines Integrations Kontopartners</span><span class="sxs-lookup"><span data-stu-id="e0f1f-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="e0f1f-114">Dieser Befehl entfernt den Integrations Kontopartner namens IntegrationAccountPartner1.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="e0f1f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0f1f-115">PARAMETERS</span></span>

### <span data-ttu-id="e0f1f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0f1f-116">-DefaultProfile</span></span>
<span data-ttu-id="e0f1f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e0f1f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0f1f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e0f1f-118">-Force</span></span>
<span data-ttu-id="e0f1f-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e0f1f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e0f1f-120">-Name</span></span>
<span data-ttu-id="e0f1f-121">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="e0f1f-122">-Partnername</span><span class="sxs-lookup"><span data-stu-id="e0f1f-122">-PartnerName</span></span>
<span data-ttu-id="e0f1f-123">Gibt den Namen des Integrations Kontopartners an.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="e0f1f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0f1f-124">-ResourceGroupName</span></span>
<span data-ttu-id="e0f1f-125">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e0f1f-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e0f1f-126">-Confirm</span></span>
<span data-ttu-id="e0f1f-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0f1f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0f1f-128">-WhatIf</span></span>
<span data-ttu-id="e0f1f-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0f1f-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0f1f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f1f-131">CommonParameters</span></span>
<span data-ttu-id="e0f1f-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0f1f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0f1f-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0f1f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f1f-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e0f1f-134">INPUTS</span></span>

### <span data-ttu-id="e0f1f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e0f1f-135">System.String</span></span>

## <span data-ttu-id="e0f1f-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e0f1f-136">OUTPUTS</span></span>

### <span data-ttu-id="e0f1f-137">System. void</span><span class="sxs-lookup"><span data-stu-id="e0f1f-137">System.Void</span></span>

## <span data-ttu-id="e0f1f-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="e0f1f-138">NOTES</span></span>

## <span data-ttu-id="e0f1f-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e0f1f-139">RELATED LINKS</span></span>

[<span data-ttu-id="e0f1f-140">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="e0f1f-140">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="e0f1f-141">Neu – AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="e0f1f-141">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="e0f1f-142">Satz-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="e0f1f-142">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


