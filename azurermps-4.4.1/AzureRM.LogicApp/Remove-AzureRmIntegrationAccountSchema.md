---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: fc7acc34a018361b3ebaff67e57221c250e19771
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663920"
---
# <span data-ttu-id="b4b5a-101">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="b4b5a-101">Remove-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="b4b5a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b5a-103">Entfernt ein Schema des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-103">Removes an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4b5a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4b5a-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4b5a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="b4b5a-106">Das Cmdlet **Remove-AzureRmIntegrationAccountSchema** entfernt ein Schema eines Integrations Kontos aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-106">The **Remove-AzureRmIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="b4b5a-107">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Schemanamen an.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-107">Specifying the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="b4b5a-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b4b5a-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b4b5a-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b4b5a-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b4b5a-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4b5a-112">EXAMPLES</span></span>

### <span data-ttu-id="b4b5a-113">Beispiel 1: Entfernen eines Schemas für ein Integrations Konto</span><span class="sxs-lookup"><span data-stu-id="b4b5a-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="b4b5a-114">Dieser Befehl entfernt ein Schema des Integrations Kontos mit dem Namen IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="b4b5a-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4b5a-115">PARAMETERS</span></span>

### <span data-ttu-id="b4b5a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b4b5a-116">-Force</span></span>
<span data-ttu-id="b4b5a-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b4b5a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b4b5a-118">-Name</span></span>
<span data-ttu-id="b4b5a-119">Gibt den Namen des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-119">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="b4b5a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4b5a-120">-ResourceGroupName</span></span>
<span data-ttu-id="b4b5a-121">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b4b5a-122">-Schemaname</span><span class="sxs-lookup"><span data-stu-id="b4b5a-122">-SchemaName</span></span>
<span data-ttu-id="b4b5a-123">Gibt den Namen eines Schemas für ein Integrations Konto an.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-123">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="b4b5a-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b4b5a-124">-Confirm</span></span>
<span data-ttu-id="b4b5a-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4b5a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4b5a-126">-WhatIf</span></span>
<span data-ttu-id="b4b5a-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4b5a-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4b5a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4b5a-129">-DefaultProfile</span></span>
<span data-ttu-id="b4b5a-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4b5a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b5a-131">CommonParameters</span></span>
<span data-ttu-id="b4b5a-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4b5a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b5a-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4b5a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b5a-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4b5a-134">INPUTS</span></span>

## <span data-ttu-id="b4b5a-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4b5a-135">OUTPUTS</span></span>

## <span data-ttu-id="b4b5a-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4b5a-136">NOTES</span></span>

## <span data-ttu-id="b4b5a-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4b5a-137">RELATED LINKS</span></span>

[<span data-ttu-id="b4b5a-138">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="b4b5a-138">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="b4b5a-139">Neu – AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="b4b5a-139">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="b4b5a-140">Satz-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="b4b5a-140">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


