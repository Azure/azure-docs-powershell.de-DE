---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 5b8da61caf8e3a89572f2054aea101a1ad8b70c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995139"
---
# <span data-ttu-id="79a6d-101">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="79a6d-101">Set-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="79a6d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="79a6d-103">Ändert ein Integrations Kontozertifikat.</span><span class="sxs-lookup"><span data-stu-id="79a6d-103">Modifies an integration account certificate.</span></span>

## <span data-ttu-id="79a6d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79a6d-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79a6d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79a6d-105">DESCRIPTION</span></span>
<span data-ttu-id="79a6d-106">Das Cmdlet " **Satz-AzIntegrationAccountCertificate** " ändert ein Integrations Kontozertifikat.</span><span class="sxs-lookup"><span data-stu-id="79a6d-106">The **Set-AzIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="79a6d-107">Dieses Cmdlet gibt ein Objekt zurück, das das Integrations Kontozertifikat darstellt.</span><span class="sxs-lookup"><span data-stu-id="79a6d-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="79a6d-108">Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Zertifikatsnamen an.</span><span class="sxs-lookup"><span data-stu-id="79a6d-108">Specifying the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="79a6d-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="79a6d-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="79a6d-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="79a6d-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="79a6d-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="79a6d-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="79a6d-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="79a6d-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="79a6d-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79a6d-113">EXAMPLES</span></span>

### <span data-ttu-id="79a6d-114">Beispiel 1: Ändern eines Integrations Kontozertifikats</span><span class="sxs-lookup"><span data-stu-id="79a6d-114">Example 1: Modify an integration account certificate</span></span>
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

<span data-ttu-id="79a6d-115">Mit diesem Befehl wird das Integrations Kontozertifikat in der angegebenen Ressourcengruppe geändert.</span><span class="sxs-lookup"><span data-stu-id="79a6d-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="79a6d-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="79a6d-116">PARAMETERS</span></span>

### <span data-ttu-id="79a6d-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="79a6d-117">-CertificateName</span></span>
<span data-ttu-id="79a6d-118">Gibt den Namen eines Integrations Kontozertifikats an.</span><span class="sxs-lookup"><span data-stu-id="79a6d-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="79a6d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a6d-119">-DefaultProfile</span></span>
<span data-ttu-id="79a6d-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="79a6d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79a6d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="79a6d-121">-Force</span></span>
<span data-ttu-id="79a6d-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="79a6d-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="79a6d-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="79a6d-123">-KeyName</span></span>
<span data-ttu-id="79a6d-124">Gibt den Namen eines Zertifikatschlüssels im schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="79a6d-124">Specifies the name of a certificate key in the key vault.</span></span>

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

### <span data-ttu-id="79a6d-125">-Keyvault-Nr.</span><span class="sxs-lookup"><span data-stu-id="79a6d-125">-KeyVaultId</span></span>
<span data-ttu-id="79a6d-126">Gibt eine schlüsseltresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="79a6d-126">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="79a6d-127">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="79a6d-127">-KeyVersion</span></span>
<span data-ttu-id="79a6d-128">Gibt die Version des Zertifikatschlüssels im schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="79a6d-128">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="79a6d-129">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="79a6d-129">-Metadata</span></span>
<span data-ttu-id="79a6d-130">Gibt ein Metadatenobjekt für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="79a6d-130">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="79a6d-131">-Name</span><span class="sxs-lookup"><span data-stu-id="79a6d-131">-Name</span></span>
<span data-ttu-id="79a6d-132">Gibt den Namen des Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="79a6d-132">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="79a6d-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="79a6d-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="79a6d-134">Gibt den Pfad einer öffentlichen Zertifikatdatei (CER) an.</span><span class="sxs-lookup"><span data-stu-id="79a6d-134">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="79a6d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79a6d-135">-ResourceGroupName</span></span>
<span data-ttu-id="79a6d-136">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="79a6d-136">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="79a6d-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="79a6d-137">-Confirm</span></span>
<span data-ttu-id="79a6d-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79a6d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79a6d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79a6d-139">-WhatIf</span></span>
<span data-ttu-id="79a6d-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79a6d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79a6d-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79a6d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79a6d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a6d-142">CommonParameters</span></span>
<span data-ttu-id="79a6d-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79a6d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a6d-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79a6d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a6d-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79a6d-145">INPUTS</span></span>

### <span data-ttu-id="79a6d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="79a6d-146">System.String</span></span>

## <span data-ttu-id="79a6d-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79a6d-147">OUTPUTS</span></span>

### <span data-ttu-id="79a6d-148">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="79a6d-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="79a6d-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="79a6d-149">NOTES</span></span>

## <span data-ttu-id="79a6d-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79a6d-150">RELATED LINKS</span></span>

[<span data-ttu-id="79a6d-151">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="79a6d-151">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="79a6d-152">Neu – AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="79a6d-152">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="79a6d-153">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="79a6d-153">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)


