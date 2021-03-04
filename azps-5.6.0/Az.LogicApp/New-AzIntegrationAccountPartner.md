---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
ms.openlocfilehash: 7b07a07dc99efa7f0f3fdb150c902b86b374181e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921955"
---
# <span data-ttu-id="1b496-101">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="1b496-101">New-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="1b496-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b496-102">SYNOPSIS</span></span>
<span data-ttu-id="1b496-103">Erstellt einen Integrationskontopartner.</span><span class="sxs-lookup"><span data-stu-id="1b496-103">Creates an integration account partner.</span></span>

## <span data-ttu-id="1b496-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b496-104">SYNTAX</span></span>

```
New-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b496-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b496-105">DESCRIPTION</span></span>
<span data-ttu-id="1b496-106">Das **Cmdlet New-AzIntegrationAccountPartner** erstellt einen Integrationskontopartner.</span><span class="sxs-lookup"><span data-stu-id="1b496-106">The **New-AzIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="1b496-107">Dieses Cmdlet gibt ein -Objekt zurück, das den Integrationskontopartner darstellt.</span><span class="sxs-lookup"><span data-stu-id="1b496-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="1b496-108">Geben Sie den Namen des Integrationskontos, den Ressourcengruppennamen, den Partnernamen und die Partneridentitäten an.</span><span class="sxs-lookup"><span data-stu-id="1b496-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>
<span data-ttu-id="1b496-109">Werte der Vorlagenparameterdatei, die Sie in der Befehlszeile angeben, haben Vorrang vor Vorlagenparameterwerten in einem Vorlagenparameterobjekt.</span><span class="sxs-lookup"><span data-stu-id="1b496-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="1b496-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="1b496-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1b496-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="1b496-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1b496-112">Um die Namen dynamischer Parameter zu ermitteln, geben Sie nach dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="1b496-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1b496-113">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="1b496-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1b496-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1b496-114">EXAMPLES</span></span>

### <span data-ttu-id="1b496-115">Beispiel 1: Erstellen eines Integrationskontopartners</span><span class="sxs-lookup"><span data-stu-id="1b496-115">Example 1: Create an integration account partner</span></span>
```
PS C:\>New-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata           :
```

<span data-ttu-id="1b496-116">Mit diesem Befehl wird der Integrationskontopartner namens IntegrationAccountPartner22 in der angegebenen Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="1b496-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="1b496-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1b496-117">PARAMETERS</span></span>

### <span data-ttu-id="1b496-118">-BusinessId-Entitäten</span><span class="sxs-lookup"><span data-stu-id="1b496-118">-BusinessIdentities</span></span>
<span data-ttu-id="1b496-119">Gibt Geschäftsidentitäten für den Integrationskontopartner an.</span><span class="sxs-lookup"><span data-stu-id="1b496-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="1b496-120">Geben Sie eine Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="1b496-120">Specify a hash table.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b496-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b496-121">-DefaultProfile</span></span>
<span data-ttu-id="1b496-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1b496-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b496-123">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="1b496-123">-Metadata</span></span>
<span data-ttu-id="1b496-124">Gibt ein Metadatenobjekt für den Partner an.</span><span class="sxs-lookup"><span data-stu-id="1b496-124">Specifies a metadata object for the partner.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b496-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1b496-125">-Name</span></span>
<span data-ttu-id="1b496-126">Gibt den Namen eines Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="1b496-126">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="1b496-127">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="1b496-127">-PartnerName</span></span>
<span data-ttu-id="1b496-128">Gibt einen Namen für den Integrationskontopartner an.</span><span class="sxs-lookup"><span data-stu-id="1b496-128">Specifies a name for the integration account partner.</span></span>

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

### <span data-ttu-id="1b496-129">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="1b496-129">-PartnerType</span></span>
<span data-ttu-id="1b496-130">Gibt den Typ des Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="1b496-130">Specifies the type of the integration account.</span></span>
<span data-ttu-id="1b496-131">Dieser Parameter unterstützt den Typ B2B.</span><span class="sxs-lookup"><span data-stu-id="1b496-131">This parameter supports the type B2B.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b496-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b496-132">-ResourceGroupName</span></span>
<span data-ttu-id="1b496-133">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1b496-133">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1b496-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1b496-134">-Confirm</span></span>
<span data-ttu-id="1b496-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b496-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b496-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b496-136">-WhatIf</span></span>
<span data-ttu-id="1b496-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b496-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b496-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b496-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b496-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b496-139">CommonParameters</span></span>
<span data-ttu-id="1b496-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b496-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b496-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b496-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b496-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1b496-142">INPUTS</span></span>

### <span data-ttu-id="1b496-143">System.String</span><span class="sxs-lookup"><span data-stu-id="1b496-143">System.String</span></span>

## <span data-ttu-id="1b496-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1b496-144">OUTPUTS</span></span>

### <span data-ttu-id="1b496-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="1b496-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="1b496-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1b496-146">NOTES</span></span>

## <span data-ttu-id="1b496-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1b496-147">RELATED LINKS</span></span>

[<span data-ttu-id="1b496-148">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="1b496-148">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="1b496-149">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="1b496-149">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="1b496-150">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="1b496-150">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


