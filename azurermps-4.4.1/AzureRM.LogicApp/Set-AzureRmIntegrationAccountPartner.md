---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 13b82cbc7b1f83c441f1211f6ebe7aa1f8c59ea5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663911"
---
# <span data-ttu-id="12871-101">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="12871-101">Set-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="12871-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12871-102">SYNOPSIS</span></span>
<span data-ttu-id="12871-103">Ändert einen Integrations Kontopartner.</span><span class="sxs-lookup"><span data-stu-id="12871-103">Modifies an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12871-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12871-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12871-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12871-105">DESCRIPTION</span></span>
<span data-ttu-id="12871-106">Das Cmdlet " **Satz-AzureRmIntegrationAccountPartner** " ändert einen Integrations Kontopartner.</span><span class="sxs-lookup"><span data-stu-id="12871-106">The **Set-AzureRmIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="12871-107">Dieses Cmdlet gibt ein Objekt zurück, das den Integrations Kontopartner darstellt.</span><span class="sxs-lookup"><span data-stu-id="12871-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="12871-108">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Partnernamen an.</span><span class="sxs-lookup"><span data-stu-id="12871-108">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="12871-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="12871-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="12871-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="12871-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="12871-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="12871-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="12871-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="12871-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="12871-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12871-113">EXAMPLES</span></span>

### <span data-ttu-id="12871-114">Beispiel 1: Ändern eines Integrations Kontopartners</span><span class="sxs-lookup"><span data-stu-id="12871-114">Example 1: Modify an integration account partner</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="12871-115">Mit diesem Befehl wird der Integrations Kontopartner namens IntegrationAccountPartner22 in der angegebenen Ressourcengruppe geändert.</span><span class="sxs-lookup"><span data-stu-id="12871-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="12871-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="12871-116">PARAMETERS</span></span>

### <span data-ttu-id="12871-117">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="12871-117">-BusinessIdentities</span></span>
<span data-ttu-id="12871-118">Gibt geschäftsidentitäten für den Integrations Kontopartner an.</span><span class="sxs-lookup"><span data-stu-id="12871-118">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="12871-119">Geben Sie eine Hashtabelle an.</span><span class="sxs-lookup"><span data-stu-id="12871-119">Specify a hash table.</span></span>

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

### <span data-ttu-id="12871-120">-Force</span><span class="sxs-lookup"><span data-stu-id="12871-120">-Force</span></span>
<span data-ttu-id="12871-121">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="12871-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="12871-122">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="12871-122">-Metadata</span></span>
<span data-ttu-id="12871-123">Gibt ein Metadatenobjekt für den Partner an.</span><span class="sxs-lookup"><span data-stu-id="12871-123">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="12871-124">-Name</span><span class="sxs-lookup"><span data-stu-id="12871-124">-Name</span></span>
<span data-ttu-id="12871-125">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="12871-125">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="12871-126">-Partnername</span><span class="sxs-lookup"><span data-stu-id="12871-126">-PartnerName</span></span>
<span data-ttu-id="12871-127">Gibt den Namen des Integrations Kontopartners an.</span><span class="sxs-lookup"><span data-stu-id="12871-127">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="12871-128">-Partnertyp</span><span class="sxs-lookup"><span data-stu-id="12871-128">-PartnerType</span></span>
<span data-ttu-id="12871-129">Gibt den Typ des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="12871-129">Specifies the type of the integration account.</span></span>
<span data-ttu-id="12871-130">Dieser Parameter unterstützt den Typ B2B.</span><span class="sxs-lookup"><span data-stu-id="12871-130">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="12871-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12871-131">-ResourceGroupName</span></span>
<span data-ttu-id="12871-132">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="12871-132">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="12871-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12871-133">-Confirm</span></span>
<span data-ttu-id="12871-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12871-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12871-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12871-135">-WhatIf</span></span>
<span data-ttu-id="12871-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12871-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12871-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12871-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12871-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12871-138">-DefaultProfile</span></span>
<span data-ttu-id="12871-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="12871-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12871-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12871-140">CommonParameters</span></span>
<span data-ttu-id="12871-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12871-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12871-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12871-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12871-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12871-143">INPUTS</span></span>

## <span data-ttu-id="12871-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12871-144">OUTPUTS</span></span>

### <span data-ttu-id="12871-145">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="12871-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="12871-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="12871-146">NOTES</span></span>

## <span data-ttu-id="12871-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12871-147">RELATED LINKS</span></span>

[<span data-ttu-id="12871-148">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="12871-148">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="12871-149">Neu – AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="12871-149">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="12871-150">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="12871-150">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)


