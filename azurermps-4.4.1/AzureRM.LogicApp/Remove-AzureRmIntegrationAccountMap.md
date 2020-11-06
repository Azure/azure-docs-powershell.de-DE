---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: a7104f33fd2e5b9428b062bd8ac359ccabb25520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501798"
---
# <span data-ttu-id="728ba-101">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="728ba-101">Remove-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="728ba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="728ba-102">SYNOPSIS</span></span>
<span data-ttu-id="728ba-103">Entfernt eine Integration-Kontozuordnung.</span><span class="sxs-lookup"><span data-stu-id="728ba-103">Removes an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="728ba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="728ba-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="728ba-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="728ba-105">DESCRIPTION</span></span>
<span data-ttu-id="728ba-106">Das Cmdlet **Remove-AzureRmIntegrationAccountMap** entfernt eine Integration-Kontozuordnung aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="728ba-106">The **Remove-AzureRmIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="728ba-107">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Kartennamen an.</span><span class="sxs-lookup"><span data-stu-id="728ba-107">Specify the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="728ba-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="728ba-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="728ba-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="728ba-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="728ba-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="728ba-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="728ba-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="728ba-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="728ba-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="728ba-112">EXAMPLES</span></span>

### <span data-ttu-id="728ba-113">Beispiel 1: Entfernen einer Integration-Kontozuordnung</span><span class="sxs-lookup"><span data-stu-id="728ba-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="728ba-114">Dieser Befehl entfernt die Integrations Kontozuordnung mit dem Namen IntegrationAccountMap47.</span><span class="sxs-lookup"><span data-stu-id="728ba-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="728ba-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="728ba-115">PARAMETERS</span></span>

### <span data-ttu-id="728ba-116">-Force</span><span class="sxs-lookup"><span data-stu-id="728ba-116">-Force</span></span>
<span data-ttu-id="728ba-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="728ba-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="728ba-118">-MapName</span><span class="sxs-lookup"><span data-stu-id="728ba-118">-MapName</span></span>
<span data-ttu-id="728ba-119">Gibt den Namen der Integrations Kontozuordnung an.</span><span class="sxs-lookup"><span data-stu-id="728ba-119">Specifies the name of the integration account map.</span></span>

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

### <span data-ttu-id="728ba-120">-Name</span><span class="sxs-lookup"><span data-stu-id="728ba-120">-Name</span></span>
<span data-ttu-id="728ba-121">Gibt den Namen des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="728ba-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="728ba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="728ba-122">-ResourceGroupName</span></span>
<span data-ttu-id="728ba-123">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="728ba-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="728ba-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="728ba-124">-Confirm</span></span>
<span data-ttu-id="728ba-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="728ba-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="728ba-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="728ba-126">-WhatIf</span></span>
<span data-ttu-id="728ba-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="728ba-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="728ba-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="728ba-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="728ba-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="728ba-129">-DefaultProfile</span></span>
<span data-ttu-id="728ba-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="728ba-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="728ba-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="728ba-131">CommonParameters</span></span>
<span data-ttu-id="728ba-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="728ba-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="728ba-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="728ba-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="728ba-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="728ba-134">INPUTS</span></span>

## <span data-ttu-id="728ba-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="728ba-135">OUTPUTS</span></span>

## <span data-ttu-id="728ba-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="728ba-136">NOTES</span></span>

## <span data-ttu-id="728ba-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="728ba-137">RELATED LINKS</span></span>

[<span data-ttu-id="728ba-138">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="728ba-138">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="728ba-139">Neu – AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="728ba-139">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="728ba-140">Satz-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="728ba-140">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


