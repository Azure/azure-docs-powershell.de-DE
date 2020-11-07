---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 0aa7f8e425d775ff1adfe8a534c6b182311e488d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650714"
---
# <span data-ttu-id="c1c51-101">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="c1c51-101">Set-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="c1c51-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c1c51-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c51-103">Ändert ein Integrations Kontozertifikat.</span><span class="sxs-lookup"><span data-stu-id="c1c51-103">Modifies an integration account certificate.</span></span>

## <span data-ttu-id="c1c51-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1c51-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1c51-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1c51-105">DESCRIPTION</span></span>
<span data-ttu-id="c1c51-106">Das Cmdlet " **Satz-AzIntegrationAccountCertificate** " ändert ein Integrations Kontozertifikat.</span><span class="sxs-lookup"><span data-stu-id="c1c51-106">The **Set-AzIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="c1c51-107">Dieses Cmdlet gibt ein Objekt zurück, das das Integrations Kontozertifikat darstellt.</span><span class="sxs-lookup"><span data-stu-id="c1c51-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="c1c51-108">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Zertifikatsnamen an.</span><span class="sxs-lookup"><span data-stu-id="c1c51-108">Specifying the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="c1c51-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="c1c51-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c1c51-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="c1c51-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c1c51-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="c1c51-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c1c51-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="c1c51-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c1c51-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1c51-113">EXAMPLES</span></span>

### <span data-ttu-id="c1c51-114">Beispiel 1: Ändern eines Integrations Kontozertifikats</span><span class="sxs-lookup"><span data-stu-id="c1c51-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="c1c51-115">Mit diesem Befehl wird das Integrations Kontozertifikat in der angegebenen Ressourcengruppe geändert.</span><span class="sxs-lookup"><span data-stu-id="c1c51-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="c1c51-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1c51-116">PARAMETERS</span></span>

### <span data-ttu-id="c1c51-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c1c51-117">-CertificateName</span></span>
<span data-ttu-id="c1c51-118">Gibt den Namen eines Integrations Kontozertifikats an.</span><span class="sxs-lookup"><span data-stu-id="c1c51-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="c1c51-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c51-119">-DefaultProfile</span></span>
<span data-ttu-id="c1c51-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c1c51-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1c51-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c1c51-121">-Force</span></span>
<span data-ttu-id="c1c51-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c1c51-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c1c51-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c1c51-123">-KeyName</span></span>
<span data-ttu-id="c1c51-124">Gibt den Namen eines Zertifikatschlüssels im schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="c1c51-124">Specifies the name of a certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c51-125">-Keyvault-Nr.</span><span class="sxs-lookup"><span data-stu-id="c1c51-125">-KeyVaultId</span></span>
<span data-ttu-id="c1c51-126">Gibt eine schlüsseltresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="c1c51-126">Specifies a key vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c51-127">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="c1c51-127">-KeyVersion</span></span>
<span data-ttu-id="c1c51-128">Gibt die Version des Zertifikatschlüssels im schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="c1c51-128">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c51-129">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="c1c51-129">-Metadata</span></span>
<span data-ttu-id="c1c51-130">Gibt ein Metadatenobjekt für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="c1c51-130">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="c1c51-131">-Name</span><span class="sxs-lookup"><span data-stu-id="c1c51-131">-Name</span></span>
<span data-ttu-id="c1c51-132">Gibt den Namen des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="c1c51-132">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="c1c51-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="c1c51-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="c1c51-134">Gibt den Pfad einer öffentlichen Zertifikatdatei (CER) an.</span><span class="sxs-lookup"><span data-stu-id="c1c51-134">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c51-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1c51-135">-ResourceGroupName</span></span>
<span data-ttu-id="c1c51-136">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="c1c51-136">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c1c51-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c1c51-137">-Confirm</span></span>
<span data-ttu-id="c1c51-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1c51-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1c51-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1c51-139">-WhatIf</span></span>
<span data-ttu-id="c1c51-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1c51-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1c51-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1c51-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1c51-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c51-142">CommonParameters</span></span>
<span data-ttu-id="c1c51-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1c51-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c51-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1c51-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c51-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c1c51-145">INPUTS</span></span>

### <span data-ttu-id="c1c51-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c1c51-146">System.String</span></span>

## <span data-ttu-id="c1c51-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c1c51-147">OUTPUTS</span></span>

### <span data-ttu-id="c1c51-148">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="c1c51-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="c1c51-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="c1c51-149">NOTES</span></span>

## <span data-ttu-id="c1c51-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c1c51-150">RELATED LINKS</span></span>

[<span data-ttu-id="c1c51-151">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="c1c51-151">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="c1c51-152">Neu – AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="c1c51-152">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="c1c51-153">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="c1c51-153">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)


