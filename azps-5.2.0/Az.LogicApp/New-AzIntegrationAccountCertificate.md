---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 651ce1141e9a925d5571f8b70d8eecedb4a1e66d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307000"
---
# <span data-ttu-id="72f3d-101">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="72f3d-101">New-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="72f3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="72f3d-103">Erstellt ein Zertifikat für das Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="72f3d-103">Creates an integration account certificate.</span></span>

## <span data-ttu-id="72f3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72f3d-104">SYNTAX</span></span>

### <span data-ttu-id="72f3d-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="72f3d-105">PrivateKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72f3d-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="72f3d-106">PublicKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72f3d-107">Beides</span><span class="sxs-lookup"><span data-stu-id="72f3d-107">Both</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72f3d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72f3d-108">DESCRIPTION</span></span>
<span data-ttu-id="72f3d-109">Das **Cmdlet "New-AzIntegrationAccountCertificate"** erstellt ein Integrationskontozertifikat.</span><span class="sxs-lookup"><span data-stu-id="72f3d-109">The **New-AzIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="72f3d-110">Dieses Cmdlet gibt ein Objekt zurück, das das Zertifikat des Integrationskontos darstellt.</span><span class="sxs-lookup"><span data-stu-id="72f3d-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="72f3d-111">Geben Sie den Namen des Integrationskontos, den Namen der Ressourcengruppe, den Zertifikatnamen, den Schlüsselnamen, die Schlüsselversion und die Schlüsseltresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="72f3d-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="72f3d-112">Werte der Vorlagenparameterdatei, die Sie in der Befehlszeile angeben, haben Vorrang vor Vorlagenparameterwerten in einem Vorlagenparameterobjekt.</span><span class="sxs-lookup"><span data-stu-id="72f3d-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="72f3d-113">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="72f3d-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="72f3d-114">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="72f3d-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="72f3d-115">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="72f3d-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="72f3d-116">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="72f3d-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="72f3d-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="72f3d-117">EXAMPLES</span></span>

### <span data-ttu-id="72f3d-118">Beispiel 1: Erstellen eines Zertifikats für ein Integrationskonto</span><span class="sxs-lookup"><span data-stu-id="72f3d-118">Example 1: Create an integration account certificate</span></span>
```
PS C:\>New-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="72f3d-119">Mit diesem Befehl wird das Zertifikat für das Integrationskonto in der angegebenen Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="72f3d-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="72f3d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72f3d-120">PARAMETERS</span></span>

### <span data-ttu-id="72f3d-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="72f3d-121">-CertificateName</span></span>
<span data-ttu-id="72f3d-122">Gibt einen Namen für das Zertifikat für das Integrationskonto an.</span><span class="sxs-lookup"><span data-stu-id="72f3d-122">Specifies a name for the integration account certificate.</span></span>

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

### <span data-ttu-id="72f3d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72f3d-123">-DefaultProfile</span></span>
<span data-ttu-id="72f3d-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="72f3d-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72f3d-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="72f3d-125">-KeyName</span></span>
<span data-ttu-id="72f3d-126">Gibt den Namen des Zertifikatschlüssels im Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="72f3d-126">Specifies the name of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="72f3d-127">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="72f3d-127">-KeyVaultId</span></span>
<span data-ttu-id="72f3d-128">Gibt eine Schlüsseltresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="72f3d-128">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="72f3d-129">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="72f3d-129">-KeyVersion</span></span>
<span data-ttu-id="72f3d-130">Gibt die Version des Zertifikatschlüssels im Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="72f3d-130">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="72f3d-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="72f3d-131">-Metadata</span></span>
<span data-ttu-id="72f3d-132">Gibt ein Metadatenobjekt für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="72f3d-132">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="72f3d-133">-Name</span><span class="sxs-lookup"><span data-stu-id="72f3d-133">-Name</span></span>
<span data-ttu-id="72f3d-134">Gibt den Namen eines Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="72f3d-134">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="72f3d-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="72f3d-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="72f3d-136">Gibt den Pfad einer öffentlichen Zertifikatdatei (CER) an.</span><span class="sxs-lookup"><span data-stu-id="72f3d-136">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="72f3d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72f3d-137">-ResourceGroupName</span></span>
<span data-ttu-id="72f3d-138">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="72f3d-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="72f3d-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72f3d-139">-Confirm</span></span>
<span data-ttu-id="72f3d-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72f3d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72f3d-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="72f3d-141">-WhatIf</span></span>
<span data-ttu-id="72f3d-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72f3d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72f3d-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72f3d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72f3d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72f3d-144">CommonParameters</span></span>
<span data-ttu-id="72f3d-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72f3d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72f3d-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72f3d-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72f3d-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="72f3d-147">INPUTS</span></span>

### <span data-ttu-id="72f3d-148">System.String</span><span class="sxs-lookup"><span data-stu-id="72f3d-148">System.String</span></span>

## <span data-ttu-id="72f3d-149">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="72f3d-149">OUTPUTS</span></span>

### <span data-ttu-id="72f3d-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="72f3d-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="72f3d-151">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="72f3d-151">NOTES</span></span>

## <span data-ttu-id="72f3d-152">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="72f3d-152">RELATED LINKS</span></span>

[<span data-ttu-id="72f3d-153">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="72f3d-153">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="72f3d-154">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="72f3d-154">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="72f3d-155">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="72f3d-155">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


