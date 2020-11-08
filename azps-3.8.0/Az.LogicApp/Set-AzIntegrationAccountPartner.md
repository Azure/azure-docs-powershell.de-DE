---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
ms.openlocfilehash: ac66c1d28c53224fedb18000db86557c8290d41a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995126"
---
# <span data-ttu-id="837ce-101">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="837ce-101">Set-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="837ce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="837ce-102">SYNOPSIS</span></span>
<span data-ttu-id="837ce-103">Ändert einen Integrations Kontopartner.</span><span class="sxs-lookup"><span data-stu-id="837ce-103">Modifies an integration account partner.</span></span>

## <span data-ttu-id="837ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="837ce-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="837ce-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="837ce-105">DESCRIPTION</span></span>
<span data-ttu-id="837ce-106">Das Cmdlet " **Satz-AzIntegrationAccountPartner** " ändert einen Integrations Kontopartner.</span><span class="sxs-lookup"><span data-stu-id="837ce-106">The **Set-AzIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="837ce-107">Dieses Cmdlet gibt ein Objekt zurück, das den Integrations Kontopartner darstellt.</span><span class="sxs-lookup"><span data-stu-id="837ce-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="837ce-108">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Partnernamen an.</span><span class="sxs-lookup"><span data-stu-id="837ce-108">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="837ce-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="837ce-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="837ce-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="837ce-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="837ce-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="837ce-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="837ce-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="837ce-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="837ce-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="837ce-113">EXAMPLES</span></span>

### <span data-ttu-id="837ce-114">Beispiel 1: Ändern eines Integrations Kontopartners</span><span class="sxs-lookup"><span data-stu-id="837ce-114">Example 1: Modify an integration account partner</span></span>
```
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

<span data-ttu-id="837ce-115">Mit diesem Befehl wird der Integrations Kontopartner namens IntegrationAccountPartner22 in der angegebenen Ressourcengruppe geändert.</span><span class="sxs-lookup"><span data-stu-id="837ce-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="837ce-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="837ce-116">PARAMETERS</span></span>

### <span data-ttu-id="837ce-117">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="837ce-117">-BusinessIdentities</span></span>
<span data-ttu-id="837ce-118">Gibt geschäftsidentitäten für den Integrations Kontopartner an.</span><span class="sxs-lookup"><span data-stu-id="837ce-118">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="837ce-119">Geben Sie eine Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="837ce-119">Specify a hash table.</span></span>

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

### <span data-ttu-id="837ce-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="837ce-120">-DefaultProfile</span></span>
<span data-ttu-id="837ce-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="837ce-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="837ce-122">-Force</span><span class="sxs-lookup"><span data-stu-id="837ce-122">-Force</span></span>
<span data-ttu-id="837ce-123">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="837ce-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="837ce-124">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="837ce-124">-Metadata</span></span>
<span data-ttu-id="837ce-125">Gibt ein Metadatenobjekt für den Partner an.</span><span class="sxs-lookup"><span data-stu-id="837ce-125">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="837ce-126">-Name</span><span class="sxs-lookup"><span data-stu-id="837ce-126">-Name</span></span>
<span data-ttu-id="837ce-127">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="837ce-127">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="837ce-128">-Partnername</span><span class="sxs-lookup"><span data-stu-id="837ce-128">-PartnerName</span></span>
<span data-ttu-id="837ce-129">Gibt den Namen des Integrations Kontopartners an.</span><span class="sxs-lookup"><span data-stu-id="837ce-129">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="837ce-130">-Partnertyp</span><span class="sxs-lookup"><span data-stu-id="837ce-130">-PartnerType</span></span>
<span data-ttu-id="837ce-131">Gibt den Typ des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="837ce-131">Specifies the type of the integration account.</span></span>
<span data-ttu-id="837ce-132">Dieser Parameter unterstützt den Typ B2B.</span><span class="sxs-lookup"><span data-stu-id="837ce-132">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="837ce-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="837ce-133">-ResourceGroupName</span></span>
<span data-ttu-id="837ce-134">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="837ce-134">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="837ce-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="837ce-135">-Confirm</span></span>
<span data-ttu-id="837ce-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="837ce-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="837ce-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="837ce-137">-WhatIf</span></span>
<span data-ttu-id="837ce-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="837ce-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="837ce-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="837ce-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="837ce-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="837ce-140">CommonParameters</span></span>
<span data-ttu-id="837ce-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="837ce-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="837ce-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="837ce-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="837ce-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="837ce-143">INPUTS</span></span>

### <span data-ttu-id="837ce-144">System. String</span><span class="sxs-lookup"><span data-stu-id="837ce-144">System.String</span></span>

## <span data-ttu-id="837ce-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="837ce-145">OUTPUTS</span></span>

### <span data-ttu-id="837ce-146">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="837ce-146">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="837ce-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="837ce-147">NOTES</span></span>

## <span data-ttu-id="837ce-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="837ce-148">RELATED LINKS</span></span>

[<span data-ttu-id="837ce-149">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="837ce-149">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="837ce-150">Neu – AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="837ce-150">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="837ce-151">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="837ce-151">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)


