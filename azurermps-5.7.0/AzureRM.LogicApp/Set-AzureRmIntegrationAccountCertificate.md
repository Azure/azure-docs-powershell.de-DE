---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: a0ffbc31727b7267be59b9645d99abdce1bfeae7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482877"
---
# <span data-ttu-id="21847-101">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="21847-101">Set-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="21847-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21847-102">SYNOPSIS</span></span>
<span data-ttu-id="21847-103">Ändert ein Integrations Kontozertifikat.</span><span class="sxs-lookup"><span data-stu-id="21847-103">Modifies an integration account certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21847-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21847-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21847-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21847-105">DESCRIPTION</span></span>
<span data-ttu-id="21847-106">Das Cmdlet " **Satz-AzureRmIntegrationAccountCertificate** " ändert ein Integrations Kontozertifikat.</span><span class="sxs-lookup"><span data-stu-id="21847-106">The **Set-AzureRmIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="21847-107">Dieses Cmdlet gibt ein Objekt zurück, das das Integrations Kontozertifikat darstellt.</span><span class="sxs-lookup"><span data-stu-id="21847-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="21847-108">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Zertifikatsnamen an.</span><span class="sxs-lookup"><span data-stu-id="21847-108">Specifying the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="21847-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="21847-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="21847-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="21847-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="21847-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="21847-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="21847-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="21847-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="21847-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21847-113">EXAMPLES</span></span>

### <span data-ttu-id="21847-114">Beispiel 1: Ändern eines Integrations Kontozertifikats</span><span class="sxs-lookup"><span data-stu-id="21847-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegartionAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="21847-115">Mit diesem Befehl wird das Integrations Kontozertifikat in der angegebenen Ressourcengruppe geändert.</span><span class="sxs-lookup"><span data-stu-id="21847-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="21847-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="21847-116">PARAMETERS</span></span>

### <span data-ttu-id="21847-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="21847-117">-CertificateName</span></span>
<span data-ttu-id="21847-118">Gibt den Namen eines Integrations Kontozertifikats an.</span><span class="sxs-lookup"><span data-stu-id="21847-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="21847-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21847-119">-DefaultProfile</span></span>
<span data-ttu-id="21847-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="21847-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21847-121">-Force</span><span class="sxs-lookup"><span data-stu-id="21847-121">-Force</span></span>
<span data-ttu-id="21847-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="21847-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="21847-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="21847-123">-KeyName</span></span>
<span data-ttu-id="21847-124">Gibt den Namen eines Zertifikatschlüssels im schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="21847-124">Specifies the name of a certificate key in the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21847-125">-Keyvault-Nr.</span><span class="sxs-lookup"><span data-stu-id="21847-125">-KeyVaultId</span></span>
<span data-ttu-id="21847-126">Gibt eine schlüsseltresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="21847-126">Specifies a key vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21847-127">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="21847-127">-KeyVersion</span></span>
<span data-ttu-id="21847-128">Gibt die Version des Zertifikatschlüssels im schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="21847-128">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21847-129">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="21847-129">-Metadata</span></span>
<span data-ttu-id="21847-130">Gibt ein Metadatenobjekt für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="21847-130">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="21847-131">-Name</span><span class="sxs-lookup"><span data-stu-id="21847-131">-Name</span></span>
<span data-ttu-id="21847-132">Gibt den Namen des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="21847-132">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="21847-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="21847-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="21847-134">Gibt den Pfad einer öffentlichen Zertifikatdatei (CER) an.</span><span class="sxs-lookup"><span data-stu-id="21847-134">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21847-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21847-135">-ResourceGroupName</span></span>
<span data-ttu-id="21847-136">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="21847-136">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="21847-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="21847-137">-Confirm</span></span>
<span data-ttu-id="21847-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21847-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21847-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21847-139">-WhatIf</span></span>
<span data-ttu-id="21847-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21847-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21847-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21847-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21847-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21847-142">CommonParameters</span></span>
<span data-ttu-id="21847-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21847-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21847-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21847-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21847-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21847-145">INPUTS</span></span>

### <span data-ttu-id="21847-146">Keine</span><span class="sxs-lookup"><span data-stu-id="21847-146">None</span></span>
<span data-ttu-id="21847-147">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="21847-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="21847-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21847-148">OUTPUTS</span></span>

### <span data-ttu-id="21847-149">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="21847-149">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="21847-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="21847-150">NOTES</span></span>

## <span data-ttu-id="21847-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21847-151">RELATED LINKS</span></span>

[<span data-ttu-id="21847-152">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="21847-152">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="21847-153">Neu – AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="21847-153">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="21847-154">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="21847-154">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)


