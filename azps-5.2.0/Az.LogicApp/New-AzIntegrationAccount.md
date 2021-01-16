---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
ms.openlocfilehash: a3a3fc16b253235da82626ab6d827d074f05860d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294725"
---
# <span data-ttu-id="73eaa-101">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="73eaa-101">New-AzIntegrationAccount</span></span>

## <span data-ttu-id="73eaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="73eaa-103">Erstellt ein Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="73eaa-103">Creates an integration account.</span></span>

## <span data-ttu-id="73eaa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73eaa-104">SYNTAX</span></span>

```
New-AzIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73eaa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73eaa-105">DESCRIPTION</span></span>
<span data-ttu-id="73eaa-106">Das **Cmdlet "New-AzIntegrationAccount"** erstellt ein Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="73eaa-106">The **New-AzIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="73eaa-107">Dieses Cmdlet gibt ein Objekt zurück, das das Integrationskonto darstellt. Geben Sie einen Namen, einen Ort, einen Ressourcengruppennamen und einen Namen für die SKU an.</span><span class="sxs-lookup"><span data-stu-id="73eaa-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>
<span data-ttu-id="73eaa-108">Werte der Vorlagenparameterdatei, die Sie in der Befehlszeile angeben, haben Vorrang vor Vorlagenparameterwerten in einem Vorlagenparameterobjekt.</span><span class="sxs-lookup"><span data-stu-id="73eaa-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="73eaa-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="73eaa-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="73eaa-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="73eaa-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="73eaa-111">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="73eaa-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="73eaa-112">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="73eaa-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="73eaa-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="73eaa-113">EXAMPLES</span></span>

### <span data-ttu-id="73eaa-114">Beispiel 1: Erstellen eines Integrationskontos</span><span class="sxs-lookup"><span data-stu-id="73eaa-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="73eaa-115">Mit diesem Befehl wird ein Integrationskonto namens "IntegrationAccount31" in der angegebenen Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="73eaa-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="73eaa-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73eaa-116">PARAMETERS</span></span>

### <span data-ttu-id="73eaa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73eaa-117">-DefaultProfile</span></span>
<span data-ttu-id="73eaa-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="73eaa-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73eaa-119">-Location</span><span class="sxs-lookup"><span data-stu-id="73eaa-119">-Location</span></span>
<span data-ttu-id="73eaa-120">Gibt einen Speicherort für das Integrationskonto an.</span><span class="sxs-lookup"><span data-stu-id="73eaa-120">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="73eaa-121">-Name</span><span class="sxs-lookup"><span data-stu-id="73eaa-121">-Name</span></span>
<span data-ttu-id="73eaa-122">Gibt einen Namen für das Integrationskonto an.</span><span class="sxs-lookup"><span data-stu-id="73eaa-122">Specifies a name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73eaa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73eaa-123">-ResourceGroupName</span></span>
<span data-ttu-id="73eaa-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="73eaa-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="73eaa-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="73eaa-125">-Sku</span></span>
<span data-ttu-id="73eaa-126">Gibt einen Namen der SKU für das Integrationskonto an.</span><span class="sxs-lookup"><span data-stu-id="73eaa-126">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73eaa-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73eaa-127">-Confirm</span></span>
<span data-ttu-id="73eaa-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="73eaa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73eaa-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="73eaa-129">-WhatIf</span></span>
<span data-ttu-id="73eaa-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73eaa-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73eaa-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73eaa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73eaa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73eaa-132">CommonParameters</span></span>
<span data-ttu-id="73eaa-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73eaa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73eaa-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73eaa-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73eaa-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="73eaa-135">INPUTS</span></span>

### <span data-ttu-id="73eaa-136">System.String</span><span class="sxs-lookup"><span data-stu-id="73eaa-136">System.String</span></span>

## <span data-ttu-id="73eaa-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="73eaa-137">OUTPUTS</span></span>

### <span data-ttu-id="73eaa-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="73eaa-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="73eaa-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="73eaa-139">NOTES</span></span>

## <span data-ttu-id="73eaa-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="73eaa-140">RELATED LINKS</span></span>

[<span data-ttu-id="73eaa-141">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="73eaa-141">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="73eaa-142">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="73eaa-142">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="73eaa-143">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="73eaa-143">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


