---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 838191018c50856f92f82699f7ac54686f1b3d97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663254"
---
# <span data-ttu-id="73c13-101">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="73c13-101">New-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="73c13-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="73c13-102">SYNOPSIS</span></span>
<span data-ttu-id="73c13-103">Erstellt eine Integrations Kontovereinbarung.</span><span class="sxs-lookup"><span data-stu-id="73c13-103">Creates an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73c13-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="73c13-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73c13-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73c13-105">DESCRIPTION</span></span>
<span data-ttu-id="73c13-106">Das Cmdlet **New-AzureRmIntegrationAccountAgreement** erstellt eine Integrations Kontovereinbarung.</span><span class="sxs-lookup"><span data-stu-id="73c13-106">The **New-AzureRmIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="73c13-107">Dieses Cmdlet gibt ein Objekt zurück, das die Integrations Kontovereinbarung darstellt.</span><span class="sxs-lookup"><span data-stu-id="73c13-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="73c13-108">Geben Sie den Namen des Integrations Kontos, den Namen der Ressourcengruppe, den Namen der Vereinbarung, den Typ, den Partnernamen, die Partner Qualifizierer und den Vertragsinhalt an.</span><span class="sxs-lookup"><span data-stu-id="73c13-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>

<span data-ttu-id="73c13-109">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="73c13-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="73c13-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="73c13-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="73c13-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="73c13-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="73c13-112">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="73c13-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="73c13-113">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="73c13-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="73c13-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73c13-114">EXAMPLES</span></span>

### <span data-ttu-id="73c13-115">Beispiel 1: Erstellen einer Integrations Kontovereinbarung</span><span class="sxs-lookup"><span data-stu-id="73c13-115">Example 1: Create a integration account agreement</span></span>
```
PS C:\>New-AzureRmIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/agreements/IntegrationAccountAgreement06
Name                   : IntegrationAccountAgreement06
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/26/2016 6:43:52 PM
ChangedTime            : 3/26/2016 6:43:52 PM
AgreementType          : X12
HostPartner            : HostPartner
GuestPartner           : GuestPartner
HostIdentityQualifier  : AA
HostIdentityValue      : AA
GuestIdentityQualifier : BB
GuestIdentityValue     : BB
Content                : {"AS2":null,"X12":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ","Valu
                         e":"ZZ"},"ProtocolSettings":{"ValidationSettings":{"ValidateCharacterSet":true,"CheckDuplicateInterchangeControlNumber":false,"InterchangeControlN

                         . . .
```

<span data-ttu-id="73c13-116">Mit diesem Befehl wird eine Integration-Kontovereinbarung in der angegebenen Azure-Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="73c13-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="73c13-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="73c13-117">PARAMETERS</span></span>

### <span data-ttu-id="73c13-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="73c13-118">-AgreementContent</span></span>
<span data-ttu-id="73c13-119">Gibt den Vertragsinhalt im JSON-Format (JavaScript Object Notation) für die Vereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="73c13-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="73c13-120">Geben Sie entweder diesen Parameter oder den *AgreementContentFilePath* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="73c13-120">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c13-121">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="73c13-121">-AgreementContentFilePath</span></span>
<span data-ttu-id="73c13-122">Gibt den Dateipfad der Vereinbarungs Inhalte an.</span><span class="sxs-lookup"><span data-stu-id="73c13-122">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="73c13-123">Geben Sie entweder diesen Parameter oder den *AgreementContent* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="73c13-123">Specify either this parameter or the *AgreementContent* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c13-124">-Vertragsname</span><span class="sxs-lookup"><span data-stu-id="73c13-124">-AgreementName</span></span>
<span data-ttu-id="73c13-125">Gibt einen Namen für die Integrations Kontovereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="73c13-125">Specifies a name for the integration account agreement.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73c13-126">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="73c13-126">-AgreementType</span></span>
<span data-ttu-id="73c13-127">Gibt den Typ der Integrations Kontovereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="73c13-127">Specifies the integration account agreement type.</span></span> <span data-ttu-id="73c13-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="73c13-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="73c13-129">X12</span><span class="sxs-lookup"><span data-stu-id="73c13-129">X12</span></span> 
- <span data-ttu-id="73c13-130">AS2</span><span class="sxs-lookup"><span data-stu-id="73c13-130">AS2</span></span>
- <span data-ttu-id="73c13-131">EDIFACT</span><span class="sxs-lookup"><span data-stu-id="73c13-131">Edifact</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: X12, AS2, Edifact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c13-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73c13-132">-DefaultProfile</span></span>
<span data-ttu-id="73c13-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="73c13-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c13-134">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="73c13-134">-GuestIdentityQualifier</span></span>
<span data-ttu-id="73c13-135">Gibt einen Namen Business Identity Qualifier für den Gast Partner an.</span><span class="sxs-lookup"><span data-stu-id="73c13-135">Specifies a name business identity qualifier for the guest partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c13-136">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="73c13-136">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="73c13-137">Der Integrations Konto-Vereinbarungs Wert des Gast Identitäts Qualifizierers.</span><span class="sxs-lookup"><span data-stu-id="73c13-137">The integration account agreement guest identity qualifier value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c13-138">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="73c13-138">-GuestPartner</span></span>
<span data-ttu-id="73c13-139">Gibt den Namen des Gast Partners an.</span><span class="sxs-lookup"><span data-stu-id="73c13-139">Specifies the name of the guest partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c13-140">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="73c13-140">-HostIdentityQualifier</span></span>
<span data-ttu-id="73c13-141">Gibt einen Namen Business Identity Qualifier für den Host Partner an.</span><span class="sxs-lookup"><span data-stu-id="73c13-141">Specifies a name business identity qualifier for the host partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c13-142">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="73c13-142">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="73c13-143">Der Integrations Kontovereinbarung-Wert des Host Identitäts Qualifizierers.</span><span class="sxs-lookup"><span data-stu-id="73c13-143">The integration account agreement host identity qualifier value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c13-144">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="73c13-144">-HostPartner</span></span>
<span data-ttu-id="73c13-145">Gibt den Namen des Host Partners an.</span><span class="sxs-lookup"><span data-stu-id="73c13-145">Specifies the name of the host partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c13-146">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="73c13-146">-Metadata</span></span>
<span data-ttu-id="73c13-147">Gibt ein Metadaten-Objekt für die Vereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="73c13-147">Specifies a metadata object for the agreement.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c13-148">-Name</span><span class="sxs-lookup"><span data-stu-id="73c13-148">-Name</span></span>
<span data-ttu-id="73c13-149">Gibt den Namen des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="73c13-149">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73c13-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73c13-150">-ResourceGroupName</span></span>
<span data-ttu-id="73c13-151">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="73c13-151">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73c13-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="73c13-152">-Confirm</span></span>
<span data-ttu-id="73c13-153">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="73c13-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c13-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73c13-154">-WhatIf</span></span>
<span data-ttu-id="73c13-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73c13-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73c13-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73c13-156">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c13-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c13-157">CommonParameters</span></span>
<span data-ttu-id="73c13-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73c13-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c13-159">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73c13-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c13-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="73c13-160">INPUTS</span></span>

### <span data-ttu-id="73c13-161">Keine</span><span class="sxs-lookup"><span data-stu-id="73c13-161">None</span></span>
<span data-ttu-id="73c13-162">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="73c13-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="73c13-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="73c13-163">OUTPUTS</span></span>

### <span data-ttu-id="73c13-164">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="73c13-164">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="73c13-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="73c13-165">NOTES</span></span>

## <span data-ttu-id="73c13-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="73c13-166">RELATED LINKS</span></span>

[<span data-ttu-id="73c13-167">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="73c13-167">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="73c13-168">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="73c13-168">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="73c13-169">Satz-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="73c13-169">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


