---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
ms.openlocfilehash: 3cff504abacedfe99052932ef1dbb7c50bf579a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948635"
---
# <span data-ttu-id="21c08-101">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="21c08-101">Set-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="21c08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21c08-102">SYNOPSIS</span></span>
<span data-ttu-id="21c08-103">Ändert einen Integrationskontopartner.</span><span class="sxs-lookup"><span data-stu-id="21c08-103">Modifies an integration account partner.</span></span>

## <span data-ttu-id="21c08-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21c08-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21c08-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21c08-105">DESCRIPTION</span></span>
<span data-ttu-id="21c08-106">Das **Cmdlet Set-AzIntegrationAccountPartner** ändert einen Integrationskontopartner.</span><span class="sxs-lookup"><span data-stu-id="21c08-106">The **Set-AzIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="21c08-107">Dieses Cmdlet gibt ein -Objekt zurück, das den Integrationskontopartner darstellt.</span><span class="sxs-lookup"><span data-stu-id="21c08-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="21c08-108">Geben Sie den Namen des Integrationskontos, den Ressourcengruppennamen und den Partnernamen an.</span><span class="sxs-lookup"><span data-stu-id="21c08-108">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="21c08-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="21c08-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="21c08-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="21c08-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="21c08-111">Um die Namen dynamischer Parameter zu ermitteln, geben Sie nach dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="21c08-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="21c08-112">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="21c08-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="21c08-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="21c08-113">EXAMPLES</span></span>

### <span data-ttu-id="21c08-114">Beispiel 1: Ändern eines Integrationskontopartners</span><span class="sxs-lookup"><span data-stu-id="21c08-114">Example 1: Modify an integration account partner</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="21c08-115">Mit diesem Befehl wird der Integrationskontopartner namens IntegrationAccountPartner22 in der angegebenen Ressourcengruppe geändert.</span><span class="sxs-lookup"><span data-stu-id="21c08-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

### <span data-ttu-id="21c08-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="21c08-116">Example 2</span></span>

<span data-ttu-id="21c08-117">Ändert einen Integrationskontopartner.</span><span class="sxs-lookup"><span data-stu-id="21c08-117">Modifies an integration account partner.</span></span> <span data-ttu-id="21c08-118">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="21c08-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountPartner -BusinessIdentities <Object> -Metadata <Object> -Name 'IntegrationAccount31' -PartnerName 'IntegrationAccountPartner22' -PartnerType B2B -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="21c08-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="21c08-119">PARAMETERS</span></span>

### <span data-ttu-id="21c08-120">-BusinessId-Entitäten</span><span class="sxs-lookup"><span data-stu-id="21c08-120">-BusinessIdentities</span></span>
<span data-ttu-id="21c08-121">Gibt Geschäftsidentitäten für den Integrationskontopartner an.</span><span class="sxs-lookup"><span data-stu-id="21c08-121">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="21c08-122">Geben Sie eine Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="21c08-122">Specify a hash table.</span></span>

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

### <span data-ttu-id="21c08-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c08-123">-DefaultProfile</span></span>
<span data-ttu-id="21c08-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="21c08-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21c08-125">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="21c08-125">-Force</span></span>
<span data-ttu-id="21c08-126">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="21c08-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="21c08-127">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="21c08-127">-Metadata</span></span>
<span data-ttu-id="21c08-128">Gibt ein Metadatenobjekt für den Partner an.</span><span class="sxs-lookup"><span data-stu-id="21c08-128">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="21c08-129">-Name</span><span class="sxs-lookup"><span data-stu-id="21c08-129">-Name</span></span>
<span data-ttu-id="21c08-130">Gibt den Namen eines Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="21c08-130">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="21c08-131">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="21c08-131">-PartnerName</span></span>
<span data-ttu-id="21c08-132">Gibt den Namen des Integrationskontopartners an.</span><span class="sxs-lookup"><span data-stu-id="21c08-132">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="21c08-133">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="21c08-133">-PartnerType</span></span>
<span data-ttu-id="21c08-134">Gibt den Typ des Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="21c08-134">Specifies the type of the integration account.</span></span>
<span data-ttu-id="21c08-135">Dieser Parameter unterstützt den Typ B2B.</span><span class="sxs-lookup"><span data-stu-id="21c08-135">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="21c08-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21c08-136">-ResourceGroupName</span></span>
<span data-ttu-id="21c08-137">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="21c08-137">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="21c08-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="21c08-138">-Confirm</span></span>
<span data-ttu-id="21c08-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21c08-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21c08-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21c08-140">-WhatIf</span></span>
<span data-ttu-id="21c08-141">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21c08-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21c08-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21c08-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21c08-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c08-143">CommonParameters</span></span>
<span data-ttu-id="21c08-144">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21c08-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c08-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21c08-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c08-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="21c08-146">INPUTS</span></span>

### <span data-ttu-id="21c08-147">System.String</span><span class="sxs-lookup"><span data-stu-id="21c08-147">System.String</span></span>

## <span data-ttu-id="21c08-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="21c08-148">OUTPUTS</span></span>

### <span data-ttu-id="21c08-149">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="21c08-149">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="21c08-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="21c08-150">NOTES</span></span>

## <span data-ttu-id="21c08-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="21c08-151">RELATED LINKS</span></span>

[<span data-ttu-id="21c08-152">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="21c08-152">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="21c08-153">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="21c08-153">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="21c08-154">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="21c08-154">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)


