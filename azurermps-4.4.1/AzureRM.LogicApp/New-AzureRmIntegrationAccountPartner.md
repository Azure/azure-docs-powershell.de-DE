---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: da4ea8acd09fadbead53d54618f04597795c45c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665371"
---
# <span data-ttu-id="90e00-101">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="90e00-101">New-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="90e00-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90e00-102">SYNOPSIS</span></span>
<span data-ttu-id="90e00-103">Erstellt einen Integrations Kontopartner.</span><span class="sxs-lookup"><span data-stu-id="90e00-103">Creates an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90e00-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90e00-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90e00-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90e00-105">DESCRIPTION</span></span>
<span data-ttu-id="90e00-106">Das Cmdlet **New-AzureRmIntegrationAccountPartner** erstellt einen Integrations Kontopartner.</span><span class="sxs-lookup"><span data-stu-id="90e00-106">The **New-AzureRmIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="90e00-107">Dieses Cmdlet gibt ein Objekt zurück, das den Integrations Kontopartner darstellt.</span><span class="sxs-lookup"><span data-stu-id="90e00-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="90e00-108">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen, den Partnernamen und die Partner Identitäten an.</span><span class="sxs-lookup"><span data-stu-id="90e00-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>

<span data-ttu-id="90e00-109">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="90e00-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="90e00-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="90e00-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="90e00-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="90e00-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="90e00-112">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="90e00-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="90e00-113">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="90e00-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="90e00-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90e00-114">EXAMPLES</span></span>

### <span data-ttu-id="90e00-115">Beispiel 1: Erstellen eines Integrations Kontopartners</span><span class="sxs-lookup"><span data-stu-id="90e00-115">Example 1: Create an integration account partner</span></span>
```
PS C:\>New-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata           :
```

<span data-ttu-id="90e00-116">Mit diesem Befehl wird der Integrations Kontopartner namens IntegrationAccountPartner22 in der angegebenen Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="90e00-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="90e00-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="90e00-117">PARAMETERS</span></span>

### <span data-ttu-id="90e00-118">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="90e00-118">-BusinessIdentities</span></span>
<span data-ttu-id="90e00-119">Gibt geschäftsidentitäten für den Integrations Kontopartner an.</span><span class="sxs-lookup"><span data-stu-id="90e00-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="90e00-120">Geben Sie eine Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="90e00-120">Specify a hash table.</span></span>

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

### <span data-ttu-id="90e00-121">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="90e00-121">-Metadata</span></span>
<span data-ttu-id="90e00-122">Gibt ein Metadatenobjekt für den Partner an.</span><span class="sxs-lookup"><span data-stu-id="90e00-122">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="90e00-123">-Name</span><span class="sxs-lookup"><span data-stu-id="90e00-123">-Name</span></span>
<span data-ttu-id="90e00-124">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="90e00-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="90e00-125">-Partnername</span><span class="sxs-lookup"><span data-stu-id="90e00-125">-PartnerName</span></span>
<span data-ttu-id="90e00-126">Gibt einen Namen für den Integrations Kontopartner an.</span><span class="sxs-lookup"><span data-stu-id="90e00-126">Specifies a name for the integration account partner.</span></span>

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

### <span data-ttu-id="90e00-127">-Partnertyp</span><span class="sxs-lookup"><span data-stu-id="90e00-127">-PartnerType</span></span>
<span data-ttu-id="90e00-128">Gibt den Typ des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="90e00-128">Specifies the type of the integration account.</span></span>
<span data-ttu-id="90e00-129">Dieser Parameter unterstützt den Typ B2B.</span><span class="sxs-lookup"><span data-stu-id="90e00-129">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="90e00-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e00-130">-ResourceGroupName</span></span>
<span data-ttu-id="90e00-131">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="90e00-131">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="90e00-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="90e00-132">-Confirm</span></span>
<span data-ttu-id="90e00-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90e00-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90e00-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90e00-134">-WhatIf</span></span>
<span data-ttu-id="90e00-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90e00-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90e00-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90e00-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90e00-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e00-137">-DefaultProfile</span></span>
<span data-ttu-id="90e00-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="90e00-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90e00-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e00-139">CommonParameters</span></span>
<span data-ttu-id="90e00-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90e00-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e00-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90e00-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e00-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90e00-142">INPUTS</span></span>

## <span data-ttu-id="90e00-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90e00-143">OUTPUTS</span></span>

### <span data-ttu-id="90e00-144">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="90e00-144">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="90e00-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="90e00-145">NOTES</span></span>

## <span data-ttu-id="90e00-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90e00-146">RELATED LINKS</span></span>

[<span data-ttu-id="90e00-147">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="90e00-147">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="90e00-148">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="90e00-148">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="90e00-149">Satz-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="90e00-149">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


