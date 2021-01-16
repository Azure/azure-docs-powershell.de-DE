---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
ms.openlocfilehash: 1daffb4bd4c6f78c0022057faa3bef052531dd46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295403"
---
# <span data-ttu-id="66b5a-101">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="66b5a-101">Remove-AzIntegrationAccount</span></span>

## <span data-ttu-id="66b5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="66b5a-103">Entfernt ein Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="66b5a-103">Removes an integration account.</span></span>

## <span data-ttu-id="66b5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66b5a-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66b5a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="66b5a-106">Das **Cmdlet "Remove-AzIntegrationAccount"** entfernt ein Integrationskonto aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="66b5a-106">The **Remove-AzIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="66b5a-107">Geben Sie den Namen des Integrationskontos und den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="66b5a-107">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="66b5a-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="66b5a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="66b5a-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="66b5a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="66b5a-110">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="66b5a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="66b5a-111">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="66b5a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="66b5a-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="66b5a-112">EXAMPLES</span></span>

### <span data-ttu-id="66b5a-113">Beispiel 1: Entfernen eines Integrationskontos</span><span class="sxs-lookup"><span data-stu-id="66b5a-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="66b5a-114">Mit diesem Befehl wird ein Integrationskonto namens "IntegrationAccount31" entfernt.</span><span class="sxs-lookup"><span data-stu-id="66b5a-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="66b5a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66b5a-115">PARAMETERS</span></span>

### <span data-ttu-id="66b5a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b5a-116">-DefaultProfile</span></span>
<span data-ttu-id="66b5a-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="66b5a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66b5a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="66b5a-118">-Force</span></span>
<span data-ttu-id="66b5a-119">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="66b5a-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66b5a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="66b5a-120">-Name</span></span>
<span data-ttu-id="66b5a-121">Gibt den Namen des Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="66b5a-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="66b5a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66b5a-122">-ResourceGroupName</span></span>
<span data-ttu-id="66b5a-123">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="66b5a-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="66b5a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66b5a-124">-Confirm</span></span>
<span data-ttu-id="66b5a-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66b5a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66b5a-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="66b5a-126">-WhatIf</span></span>
<span data-ttu-id="66b5a-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66b5a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66b5a-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66b5a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66b5a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b5a-129">CommonParameters</span></span>
<span data-ttu-id="66b5a-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66b5a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b5a-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66b5a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b5a-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="66b5a-132">INPUTS</span></span>

### <span data-ttu-id="66b5a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="66b5a-133">System.String</span></span>

## <span data-ttu-id="66b5a-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="66b5a-134">OUTPUTS</span></span>

### <span data-ttu-id="66b5a-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="66b5a-135">System.Void</span></span>

## <span data-ttu-id="66b5a-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="66b5a-136">NOTES</span></span>

## <span data-ttu-id="66b5a-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="66b5a-137">RELATED LINKS</span></span>

[<span data-ttu-id="66b5a-138">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="66b5a-138">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="66b5a-139">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="66b5a-139">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

[<span data-ttu-id="66b5a-140">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="66b5a-140">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)


