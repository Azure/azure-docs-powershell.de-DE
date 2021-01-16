---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 190745ce8b09bf29b3cc3cbc07f35899732f97f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290080"
---
# <span data-ttu-id="0eb5f-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="0eb5f-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="0eb5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eb5f-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb5f-103">Erstellt einen Integrationskontovertrag.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="0eb5f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0eb5f-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0eb5f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0eb5f-105">DESCRIPTION</span></span>
<span data-ttu-id="0eb5f-106">Das **Cmdlet "New-AzIntegrationAccountAgreement"** erstellt einen Integrationskontovertrag.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="0eb5f-107">Dieses Cmdlet gibt ein Objekt zurück, das den Vertrag für das Integrationskonto darstellt.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="0eb5f-108">Geben Sie den Namen des Integrationskontos, den Namen der Ressourcengruppe, den Vertragsnamen, den Typ, den Partnernamen, Partnerqualifizierer und Vertragsinhalt an.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="0eb5f-109">Werte der Vorlagenparameterdatei, die Sie in der Befehlszeile angeben, haben Vorrang vor Vorlagenparameterwerten in einem Vorlagenparameterobjekt.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="0eb5f-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0eb5f-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0eb5f-112">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0eb5f-113">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0eb5f-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0eb5f-114">EXAMPLES</span></span>

### <span data-ttu-id="0eb5f-115">Beispiel 1: Erstellen eines Vertrags für ein Integrationskonto</span><span class="sxs-lookup"><span data-stu-id="0eb5f-115">Example 1: Create a integration account agreement</span></span>
```powershell
PS C:\>New-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="0eb5f-116">Mit diesem Befehl wird eine Vereinbarung für ein Integrationskonto in der angegebenen Azure-Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="0eb5f-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0eb5f-117">Example 2</span></span>

<span data-ttu-id="0eb5f-118">Erstellt einen Integrationskontovertrag.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-118">Creates an integration account agreement.</span></span> <span data-ttu-id="0eb5f-119">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="0eb5f-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountAgreement -AgreementContent <String> -AgreementName 'IntegrationAccountAgreement06' -AgreementType X12 -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="0eb5f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0eb5f-120">PARAMETERS</span></span>

### <span data-ttu-id="0eb5f-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="0eb5f-121">-AgreementContent</span></span>
<span data-ttu-id="0eb5f-122">Gibt Vertragsinhalt im JavaScript Object Notation (JSON)-Format für den Vertrag an.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="0eb5f-123">Geben Sie entweder diesen Parameter oder den *Parameter "AgreementContentFilePath"* an.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-123">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb5f-124">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="0eb5f-124">-AgreementContentFilePath</span></span>
<span data-ttu-id="0eb5f-125">Gibt den Dateipfad des Vertragsinhalts für den Vertrag an.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-125">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="0eb5f-126">Geben Sie entweder diesen Parameter oder den *Parameter "AgreementContent"* an.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-126">Specify either this parameter or the *AgreementContent* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb5f-127">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="0eb5f-127">-AgreementName</span></span>
<span data-ttu-id="0eb5f-128">Gibt einen Namen für die Vereinbarung für das Integrationskonto an.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-128">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="0eb5f-129">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="0eb5f-129">-AgreementType</span></span>
<span data-ttu-id="0eb5f-130">Gibt den Typ des Vertrags für das Integrationskonto an.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-130">Specifies the integration account agreement type.</span></span> <span data-ttu-id="0eb5f-131">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="0eb5f-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0eb5f-132">X12</span><span class="sxs-lookup"><span data-stu-id="0eb5f-132">X12</span></span> 
- <span data-ttu-id="0eb5f-133">AS2</span><span class="sxs-lookup"><span data-stu-id="0eb5f-133">AS2</span></span>
- <span data-ttu-id="0eb5f-134">Edifact</span><span class="sxs-lookup"><span data-stu-id="0eb5f-134">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb5f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb5f-135">-DefaultProfile</span></span>
<span data-ttu-id="0eb5f-136">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0eb5f-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0eb5f-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="0eb5f-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="0eb5f-138">Gibt einen Namensidentitätsqualifizierer für den Gastpartner an.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="0eb5f-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="0eb5f-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="0eb5f-140">Der Wert für den Gastidentitätsqualifizierer für den Integrationskontovertrag.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="0eb5f-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="0eb5f-141">-GuestPartner</span></span>
<span data-ttu-id="0eb5f-142">Gibt den Namen des Gastpartners an.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="0eb5f-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="0eb5f-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="0eb5f-144">Gibt einen Namensidentitätsqualifizierer für den Hostpartner an.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="0eb5f-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="0eb5f-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="0eb5f-146">Der Hostidentitätsqualifiziererwert für den Integrationskontovertrag.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="0eb5f-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="0eb5f-147">-HostPartner</span></span>
<span data-ttu-id="0eb5f-148">Gibt den Namen des Hostpartners an.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="0eb5f-149">-Metadata</span><span class="sxs-lookup"><span data-stu-id="0eb5f-149">-Metadata</span></span>
<span data-ttu-id="0eb5f-150">Gibt ein Metadatenobjekt für die Vereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="0eb5f-151">-Name</span><span class="sxs-lookup"><span data-stu-id="0eb5f-151">-Name</span></span>
<span data-ttu-id="0eb5f-152">Gibt den Namen des Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-152">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="0eb5f-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eb5f-153">-ResourceGroupName</span></span>
<span data-ttu-id="0eb5f-154">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0eb5f-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0eb5f-155">-Confirm</span></span>
<span data-ttu-id="0eb5f-156">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eb5f-157">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0eb5f-157">-WhatIf</span></span>
<span data-ttu-id="0eb5f-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eb5f-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eb5f-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb5f-160">CommonParameters</span></span>
<span data-ttu-id="0eb5f-161">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eb5f-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb5f-162">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0eb5f-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb5f-163">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0eb5f-163">INPUTS</span></span>

### <span data-ttu-id="0eb5f-164">System.String</span><span class="sxs-lookup"><span data-stu-id="0eb5f-164">System.String</span></span>

## <span data-ttu-id="0eb5f-165">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0eb5f-165">OUTPUTS</span></span>

### <span data-ttu-id="0eb5f-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="0eb5f-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="0eb5f-167">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0eb5f-167">NOTES</span></span>

## <span data-ttu-id="0eb5f-168">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0eb5f-168">RELATED LINKS</span></span>

[<span data-ttu-id="0eb5f-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="0eb5f-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="0eb5f-170">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="0eb5f-170">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="0eb5f-171">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="0eb5f-171">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


