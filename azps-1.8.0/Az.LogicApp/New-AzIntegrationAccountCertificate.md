---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 2a59e10fd7cba1bd2ec164b6fa2724a97ee78694
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819343"
---
# <span data-ttu-id="24f96-101">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="24f96-101">New-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="24f96-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24f96-102">SYNOPSIS</span></span>
<span data-ttu-id="24f96-103">Erstellt ein Integrations Kontozertifikat.</span><span class="sxs-lookup"><span data-stu-id="24f96-103">Creates an integration account certificate.</span></span>

## <span data-ttu-id="24f96-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24f96-104">SYNTAX</span></span>

### <span data-ttu-id="24f96-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="24f96-105">PrivateKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24f96-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="24f96-106">PublicKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24f96-107">Sowohl</span><span class="sxs-lookup"><span data-stu-id="24f96-107">Both</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24f96-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24f96-108">DESCRIPTION</span></span>
<span data-ttu-id="24f96-109">Das Cmdlet **New-AzIntegrationAccountCertificate** erstellt ein Integrations Kontozertifikat.</span><span class="sxs-lookup"><span data-stu-id="24f96-109">The **New-AzIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="24f96-110">Dieses Cmdlet gibt ein Objekt zurück, das das Integrations Kontozertifikat darstellt.</span><span class="sxs-lookup"><span data-stu-id="24f96-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="24f96-111">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen, den Zertifikatnamen, den Schlüsselnamen, die Schlüssel Version und die schlüsseltresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="24f96-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="24f96-112">In der Befehlszeile angegebene Vorlagenparameter-Datei Werte haben Vorrang vor Vorlagenparameter Werten in einem Vorlagenparameter Objekt.</span><span class="sxs-lookup"><span data-stu-id="24f96-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="24f96-113">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="24f96-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="24f96-114">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="24f96-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="24f96-115">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="24f96-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="24f96-116">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="24f96-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="24f96-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24f96-117">EXAMPLES</span></span>

### <span data-ttu-id="24f96-118">Beispiel 1: Erstellen eines Integrations Kontozertifikats</span><span class="sxs-lookup"><span data-stu-id="24f96-118">Example 1: Create an integration account certificate</span></span>
```
PS C:\>New-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
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

<span data-ttu-id="24f96-119">Mit diesem Befehl wird das Integrations Kontozertifikat in der angegebenen Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="24f96-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="24f96-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="24f96-120">PARAMETERS</span></span>

### <span data-ttu-id="24f96-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="24f96-121">-CertificateName</span></span>
<span data-ttu-id="24f96-122">Gibt einen Namen für das Integrations Kontozertifikat an.</span><span class="sxs-lookup"><span data-stu-id="24f96-122">Specifies a name for the integration account certificate.</span></span>

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

### <span data-ttu-id="24f96-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24f96-123">-DefaultProfile</span></span>
<span data-ttu-id="24f96-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="24f96-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24f96-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="24f96-125">-KeyName</span></span>
<span data-ttu-id="24f96-126">Gibt den Namen des Zertifikatschlüssels im schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="24f96-126">Specifies the name of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24f96-127">-Keyvault-Nr.</span><span class="sxs-lookup"><span data-stu-id="24f96-127">-KeyVaultId</span></span>
<span data-ttu-id="24f96-128">Gibt eine schlüsseltresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="24f96-128">Specifies a key vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24f96-129">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="24f96-129">-KeyVersion</span></span>
<span data-ttu-id="24f96-130">Gibt die Version des Zertifikatschlüssels im schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="24f96-130">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24f96-131">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="24f96-131">-Metadata</span></span>
<span data-ttu-id="24f96-132">Gibt ein Metadatenobjekt für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="24f96-132">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="24f96-133">-Name</span><span class="sxs-lookup"><span data-stu-id="24f96-133">-Name</span></span>
<span data-ttu-id="24f96-134">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="24f96-134">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24f96-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="24f96-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="24f96-136">Gibt den Pfad einer öffentlichen Zertifikatdatei (CER) an.</span><span class="sxs-lookup"><span data-stu-id="24f96-136">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24f96-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24f96-137">-ResourceGroupName</span></span>
<span data-ttu-id="24f96-138">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="24f96-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="24f96-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="24f96-139">-Confirm</span></span>
<span data-ttu-id="24f96-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="24f96-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24f96-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24f96-141">-WhatIf</span></span>
<span data-ttu-id="24f96-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="24f96-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24f96-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="24f96-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24f96-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f96-144">CommonParameters</span></span>
<span data-ttu-id="24f96-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24f96-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f96-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24f96-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f96-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24f96-147">INPUTS</span></span>

### <span data-ttu-id="24f96-148">System. String</span><span class="sxs-lookup"><span data-stu-id="24f96-148">System.String</span></span>

## <span data-ttu-id="24f96-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24f96-149">OUTPUTS</span></span>

### <span data-ttu-id="24f96-150">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="24f96-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="24f96-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="24f96-151">NOTES</span></span>

## <span data-ttu-id="24f96-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24f96-152">RELATED LINKS</span></span>

[<span data-ttu-id="24f96-153">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="24f96-153">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="24f96-154">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="24f96-154">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="24f96-155">Satz-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="24f96-155">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


