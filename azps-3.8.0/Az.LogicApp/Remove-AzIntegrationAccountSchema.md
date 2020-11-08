---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
ms.openlocfilehash: 50eab845d20d9bf95c20e94f6309be2a302f413c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004543"
---
# <span data-ttu-id="9d269-101">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9d269-101">Remove-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="9d269-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d269-102">SYNOPSIS</span></span>
<span data-ttu-id="9d269-103">Entfernt ein Schema des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="9d269-103">Removes an integration account schema.</span></span>

## <span data-ttu-id="9d269-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d269-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d269-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d269-105">DESCRIPTION</span></span>
<span data-ttu-id="9d269-106">Das Cmdlet **Remove-AzIntegrationAccountSchema** entfernt ein Schema eines Integrations Kontos aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9d269-106">The **Remove-AzIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="9d269-107">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Schemanamen an.</span><span class="sxs-lookup"><span data-stu-id="9d269-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="9d269-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="9d269-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9d269-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="9d269-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9d269-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="9d269-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9d269-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="9d269-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9d269-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d269-112">EXAMPLES</span></span>

### <span data-ttu-id="9d269-113">Beispiel 1: Entfernen eines Schemas für ein Integrations Konto</span><span class="sxs-lookup"><span data-stu-id="9d269-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="9d269-114">Dieser Befehl entfernt ein Schema des Integrations Kontos mit dem Namen IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="9d269-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="9d269-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d269-115">PARAMETERS</span></span>

### <span data-ttu-id="9d269-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d269-116">-DefaultProfile</span></span>
<span data-ttu-id="9d269-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9d269-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d269-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9d269-118">-Force</span></span>
<span data-ttu-id="9d269-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9d269-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9d269-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9d269-120">-Name</span></span>
<span data-ttu-id="9d269-121">Gibt den Namen des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="9d269-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="9d269-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d269-122">-ResourceGroupName</span></span>
<span data-ttu-id="9d269-123">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9d269-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9d269-124">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="9d269-124">-SchemaName</span></span>
<span data-ttu-id="9d269-125">Gibt den Namen eines Schemas für ein Integrations Konto an.</span><span class="sxs-lookup"><span data-stu-id="9d269-125">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="9d269-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9d269-126">-Confirm</span></span>
<span data-ttu-id="9d269-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9d269-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d269-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d269-128">-WhatIf</span></span>
<span data-ttu-id="9d269-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9d269-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d269-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9d269-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d269-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d269-131">CommonParameters</span></span>
<span data-ttu-id="9d269-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d269-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d269-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d269-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d269-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d269-134">INPUTS</span></span>

### <span data-ttu-id="9d269-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9d269-135">System.String</span></span>

## <span data-ttu-id="9d269-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d269-136">OUTPUTS</span></span>

### <span data-ttu-id="9d269-137">System. void</span><span class="sxs-lookup"><span data-stu-id="9d269-137">System.Void</span></span>

## <span data-ttu-id="9d269-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d269-138">NOTES</span></span>

## <span data-ttu-id="9d269-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d269-139">RELATED LINKS</span></span>

[<span data-ttu-id="9d269-140">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9d269-140">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="9d269-141">Neu – AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9d269-141">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="9d269-142">Satz-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9d269-142">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


