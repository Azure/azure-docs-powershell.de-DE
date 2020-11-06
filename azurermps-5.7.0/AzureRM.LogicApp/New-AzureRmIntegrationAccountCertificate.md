---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 555da1343813884a1f773d199cb99a188f7efedc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499830"
---
# <span data-ttu-id="4a428-101">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="4a428-101">New-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="4a428-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4a428-102">SYNOPSIS</span></span>
<span data-ttu-id="4a428-103">Erstellt ein Integrations Kontozertifikat.</span><span class="sxs-lookup"><span data-stu-id="4a428-103">Creates an integration account certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a428-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a428-104">SYNTAX</span></span>

### <span data-ttu-id="4a428-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="4a428-105">PrivateKey</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a428-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="4a428-106">PublicKey</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a428-107">Sowohl</span><span class="sxs-lookup"><span data-stu-id="4a428-107">Both</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a428-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a428-108">DESCRIPTION</span></span>
<span data-ttu-id="4a428-109">Das Cmdlet **New-AzureRmIntegrationAccountCertificate** erstellt ein Integrations Kontozertifikat.</span><span class="sxs-lookup"><span data-stu-id="4a428-109">The **New-AzureRmIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="4a428-110">Dieses Cmdlet gibt ein Objekt zurück, das das Integrations Kontozertifikat darstellt.</span><span class="sxs-lookup"><span data-stu-id="4a428-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="4a428-111">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen, den Zertifikatnamen, den Schlüsselnamen, die Schlüssel Version und die schlüsseltresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="4a428-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="4a428-112">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="4a428-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="4a428-113">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="4a428-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4a428-114">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="4a428-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4a428-115">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="4a428-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4a428-116">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="4a428-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4a428-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a428-117">EXAMPLES</span></span>

### <span data-ttu-id="4a428-118">Beispiel 1: Erstellen eines Integrations Kontozertifikats</span><span class="sxs-lookup"><span data-stu-id="4a428-118">Example 1: Create an integration account certificate</span></span>
```
PS C:\>New-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="4a428-119">Mit diesem Befehl wird das Integrations Kontozertifikat in der angegebenen Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="4a428-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="4a428-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a428-120">PARAMETERS</span></span>

### <span data-ttu-id="4a428-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="4a428-121">-CertificateName</span></span>
<span data-ttu-id="4a428-122">Gibt einen Namen für das Integrations Kontozertifikat an.</span><span class="sxs-lookup"><span data-stu-id="4a428-122">Specifies a name for the integration account certificate.</span></span>

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

### <span data-ttu-id="4a428-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a428-123">-DefaultProfile</span></span>
<span data-ttu-id="4a428-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4a428-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a428-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="4a428-125">-KeyName</span></span>
<span data-ttu-id="4a428-126">Gibt den Namen des Zertifikatschlüssels im schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="4a428-126">Specifies the name of the certificate key in the key vault.</span></span>

```yaml
Type: String
Parameter Sets: PrivateKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: PublicKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a428-127">-Keyvault-Nr.</span><span class="sxs-lookup"><span data-stu-id="4a428-127">-KeyVaultId</span></span>
<span data-ttu-id="4a428-128">Gibt eine schlüsseltresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="4a428-128">Specifies a key vault ID.</span></span>

```yaml
Type: String
Parameter Sets: PrivateKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: PublicKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a428-129">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="4a428-129">-KeyVersion</span></span>
<span data-ttu-id="4a428-130">Gibt die Version des Zertifikatschlüssels im schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="4a428-130">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: String
Parameter Sets: PrivateKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: PublicKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a428-131">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="4a428-131">-Metadata</span></span>
<span data-ttu-id="4a428-132">Gibt ein Metadatenobjekt für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="4a428-132">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="4a428-133">-Name</span><span class="sxs-lookup"><span data-stu-id="4a428-133">-Name</span></span>
<span data-ttu-id="4a428-134">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="4a428-134">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a428-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="4a428-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="4a428-136">Gibt den Pfad einer öffentlichen Zertifikatdatei (CER) an.</span><span class="sxs-lookup"><span data-stu-id="4a428-136">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: String
Parameter Sets: PrivateKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: PublicKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a428-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a428-137">-ResourceGroupName</span></span>
<span data-ttu-id="4a428-138">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4a428-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4a428-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4a428-139">-Confirm</span></span>
<span data-ttu-id="4a428-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4a428-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a428-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a428-141">-WhatIf</span></span>
<span data-ttu-id="4a428-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a428-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a428-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a428-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a428-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a428-144">CommonParameters</span></span>
<span data-ttu-id="4a428-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a428-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a428-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a428-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a428-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4a428-147">INPUTS</span></span>

### <span data-ttu-id="4a428-148">Keine</span><span class="sxs-lookup"><span data-stu-id="4a428-148">None</span></span>
<span data-ttu-id="4a428-149">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4a428-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4a428-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4a428-150">OUTPUTS</span></span>

### <span data-ttu-id="4a428-151">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="4a428-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="4a428-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="4a428-152">NOTES</span></span>

## <span data-ttu-id="4a428-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4a428-153">RELATED LINKS</span></span>

[<span data-ttu-id="4a428-154">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="4a428-154">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="4a428-155">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="4a428-155">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="4a428-156">Satz-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="4a428-156">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


