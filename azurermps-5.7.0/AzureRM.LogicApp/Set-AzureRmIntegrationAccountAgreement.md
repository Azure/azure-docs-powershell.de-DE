---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 79ad0434a7918bbdf834b5917ed023cbbabf0525
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662726"
---
# <span data-ttu-id="09648-101">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="09648-101">Set-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="09648-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09648-102">SYNOPSIS</span></span>
<span data-ttu-id="09648-103">Ändert eine Integration-Kontovereinbarung.</span><span class="sxs-lookup"><span data-stu-id="09648-103">Modifies an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09648-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09648-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="09648-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09648-105">DESCRIPTION</span></span>
<span data-ttu-id="09648-106">Das Cmdlet " **Satz-AzureRmIntegrationAccountAgreement** " ändert eine Integration-Kontovereinbarung.</span><span class="sxs-lookup"><span data-stu-id="09648-106">The **Set-AzureRmIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="09648-107">Dieses Cmdlet gibt ein Objekt zurück, das die Integrations Kontovereinbarung darstellt.</span><span class="sxs-lookup"><span data-stu-id="09648-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="09648-108">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Vertragsnamen an.</span><span class="sxs-lookup"><span data-stu-id="09648-108">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="09648-109">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="09648-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="09648-110">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="09648-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="09648-111">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="09648-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="09648-112">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="09648-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="09648-113">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="09648-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="09648-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09648-114">EXAMPLES</span></span>

### <span data-ttu-id="09648-115">Beispiel 1: Aktualisieren einer Integration-Kontovereinbarung</span><span class="sxs-lookup"><span data-stu-id="09648-115">Example 1: Update an integration account agreement</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="09648-116">Dieser Befehl aktualisiert eine Integration-Kontovereinbarung in der angegebenen Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="09648-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="09648-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="09648-117">PARAMETERS</span></span>

### <span data-ttu-id="09648-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="09648-118">-AgreementContent</span></span>
<span data-ttu-id="09648-119">Gibt den Vertragsinhalt im JSON-Format (JavaScript Object Notation) für die Vereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="09648-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="09648-120">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="09648-120">-AgreementContentFilePath</span></span>
<span data-ttu-id="09648-121">Gibt den Dateipfad der Vereinbarungs Inhalte an.</span><span class="sxs-lookup"><span data-stu-id="09648-121">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="09648-122">-Vertragsname</span><span class="sxs-lookup"><span data-stu-id="09648-122">-AgreementName</span></span>
<span data-ttu-id="09648-123">Gibt den Namen der Integrations Kontovereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="09648-123">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="09648-124">-Agreementtype</span><span class="sxs-lookup"><span data-stu-id="09648-124">-AgreementType</span></span>
<span data-ttu-id="09648-125">Gibt den Typ der Integrations Kontovereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="09648-125">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="09648-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="09648-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="09648-127">X12</span><span class="sxs-lookup"><span data-stu-id="09648-127">X12</span></span> 
- <span data-ttu-id="09648-128">AS2</span><span class="sxs-lookup"><span data-stu-id="09648-128">AS2</span></span>
- <span data-ttu-id="09648-129">EDIFACT</span><span class="sxs-lookup"><span data-stu-id="09648-129">Edifact</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: X12, AS2, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09648-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09648-130">-DefaultProfile</span></span>
<span data-ttu-id="09648-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="09648-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09648-132">-Force</span><span class="sxs-lookup"><span data-stu-id="09648-132">-Force</span></span>
<span data-ttu-id="09648-133">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="09648-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09648-134">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="09648-134">-GuestIdentityQualifier</span></span>
<span data-ttu-id="09648-135">Gibt einen Namen Business Identity Qualifier für den Gast Partner an.</span><span class="sxs-lookup"><span data-stu-id="09648-135">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="09648-136">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="09648-136">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="09648-137">Der Integrations Konto-Vereinbarungs Wert des Gast Identitäts Qualifizierers.</span><span class="sxs-lookup"><span data-stu-id="09648-137">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="09648-138">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="09648-138">-GuestPartner</span></span>
<span data-ttu-id="09648-139">Gibt den Namen des Gast Partners an.</span><span class="sxs-lookup"><span data-stu-id="09648-139">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="09648-140">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="09648-140">-HostIdentityQualifier</span></span>
<span data-ttu-id="09648-141">Gibt einen Namen Business Identity Qualifier für den Host Partner an.</span><span class="sxs-lookup"><span data-stu-id="09648-141">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="09648-142">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="09648-142">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="09648-143">Der Integrations Kontovereinbarung-Wert des Host Identitäts Qualifizierers.</span><span class="sxs-lookup"><span data-stu-id="09648-143">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="09648-144">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="09648-144">-HostPartner</span></span>
<span data-ttu-id="09648-145">Gibt den Namen des Host Partners an.</span><span class="sxs-lookup"><span data-stu-id="09648-145">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="09648-146">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="09648-146">-Metadata</span></span>
<span data-ttu-id="09648-147">Gibt ein Metadaten-Objekt für die Vereinbarung an.</span><span class="sxs-lookup"><span data-stu-id="09648-147">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="09648-148">-Name</span><span class="sxs-lookup"><span data-stu-id="09648-148">-Name</span></span>
<span data-ttu-id="09648-149">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="09648-149">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="09648-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09648-150">-ResourceGroupName</span></span>
<span data-ttu-id="09648-151">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="09648-151">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="09648-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="09648-152">-Confirm</span></span>
<span data-ttu-id="09648-153">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="09648-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09648-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09648-154">-WhatIf</span></span>
<span data-ttu-id="09648-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09648-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09648-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="09648-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09648-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09648-157">CommonParameters</span></span>
<span data-ttu-id="09648-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09648-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09648-159">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09648-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09648-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09648-160">INPUTS</span></span>

### <span data-ttu-id="09648-161">Keine</span><span class="sxs-lookup"><span data-stu-id="09648-161">None</span></span>
<span data-ttu-id="09648-162">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="09648-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="09648-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09648-163">OUTPUTS</span></span>

### <span data-ttu-id="09648-164">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="09648-164">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="09648-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="09648-165">NOTES</span></span>

## <span data-ttu-id="09648-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09648-166">RELATED LINKS</span></span>

[<span data-ttu-id="09648-167">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="09648-167">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="09648-168">Neu – AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="09648-168">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="09648-169">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="09648-169">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)


