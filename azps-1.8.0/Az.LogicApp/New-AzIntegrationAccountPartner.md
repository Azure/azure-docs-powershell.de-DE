---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
ms.openlocfilehash: fe54643e3425d495a78d6a925f9518d965b77d77
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819336"
---
# <span data-ttu-id="584d9-101">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="584d9-101">New-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="584d9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="584d9-102">SYNOPSIS</span></span>
<span data-ttu-id="584d9-103">Erstellt einen Integrations Kontopartner.</span><span class="sxs-lookup"><span data-stu-id="584d9-103">Creates an integration account partner.</span></span>

## <span data-ttu-id="584d9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="584d9-104">SYNTAX</span></span>

```
New-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="584d9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="584d9-105">DESCRIPTION</span></span>
<span data-ttu-id="584d9-106">Das Cmdlet **New-AzIntegrationAccountPartner** erstellt einen Integrations Kontopartner.</span><span class="sxs-lookup"><span data-stu-id="584d9-106">The **New-AzIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="584d9-107">Dieses Cmdlet gibt ein Objekt zurück, das den Integrations Kontopartner darstellt.</span><span class="sxs-lookup"><span data-stu-id="584d9-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="584d9-108">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen, den Partnernamen und die Partner Identitäten an.</span><span class="sxs-lookup"><span data-stu-id="584d9-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>
<span data-ttu-id="584d9-109">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="584d9-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="584d9-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="584d9-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="584d9-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="584d9-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="584d9-112">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="584d9-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="584d9-113">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="584d9-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="584d9-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="584d9-114">EXAMPLES</span></span>

### <span data-ttu-id="584d9-115">Beispiel 1: Erstellen eines Integrations Kontopartners</span><span class="sxs-lookup"><span data-stu-id="584d9-115">Example 1: Create an integration account partner</span></span>
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

<span data-ttu-id="584d9-116">Mit diesem Befehl wird der Integrations Kontopartner namens IntegrationAccountPartner22 in der angegebenen Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="584d9-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="584d9-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="584d9-117">PARAMETERS</span></span>

### <span data-ttu-id="584d9-118">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="584d9-118">-BusinessIdentities</span></span>
<span data-ttu-id="584d9-119">Gibt geschäftsidentitäten für den Integrations Kontopartner an.</span><span class="sxs-lookup"><span data-stu-id="584d9-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="584d9-120">Geben Sie eine Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="584d9-120">Specify a hash table.</span></span>

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

### <span data-ttu-id="584d9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="584d9-121">-DefaultProfile</span></span>
<span data-ttu-id="584d9-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="584d9-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="584d9-123">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="584d9-123">-Metadata</span></span>
<span data-ttu-id="584d9-124">Gibt ein Metadatenobjekt für den Partner an.</span><span class="sxs-lookup"><span data-stu-id="584d9-124">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="584d9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="584d9-125">-Name</span></span>
<span data-ttu-id="584d9-126">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="584d9-126">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="584d9-127">-Partnername</span><span class="sxs-lookup"><span data-stu-id="584d9-127">-PartnerName</span></span>
<span data-ttu-id="584d9-128">Gibt einen Namen für den Integrations Kontopartner an.</span><span class="sxs-lookup"><span data-stu-id="584d9-128">Specifies a name for the integration account partner.</span></span>

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

### <span data-ttu-id="584d9-129">-Partnertyp</span><span class="sxs-lookup"><span data-stu-id="584d9-129">-PartnerType</span></span>
<span data-ttu-id="584d9-130">Gibt den Typ des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="584d9-130">Specifies the type of the integration account.</span></span>
<span data-ttu-id="584d9-131">Dieser Parameter unterstützt den Typ B2B.</span><span class="sxs-lookup"><span data-stu-id="584d9-131">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="584d9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="584d9-132">-ResourceGroupName</span></span>
<span data-ttu-id="584d9-133">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="584d9-133">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="584d9-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="584d9-134">-Confirm</span></span>
<span data-ttu-id="584d9-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="584d9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="584d9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="584d9-136">-WhatIf</span></span>
<span data-ttu-id="584d9-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="584d9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="584d9-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="584d9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="584d9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="584d9-139">CommonParameters</span></span>
<span data-ttu-id="584d9-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="584d9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="584d9-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="584d9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="584d9-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="584d9-142">INPUTS</span></span>

### <span data-ttu-id="584d9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="584d9-143">System.String</span></span>

## <span data-ttu-id="584d9-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="584d9-144">OUTPUTS</span></span>

### <span data-ttu-id="584d9-145">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="584d9-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="584d9-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="584d9-146">NOTES</span></span>

## <span data-ttu-id="584d9-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="584d9-147">RELATED LINKS</span></span>

[<span data-ttu-id="584d9-148">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="584d9-148">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="584d9-149">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="584d9-149">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="584d9-150">Satz-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="584d9-150">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


