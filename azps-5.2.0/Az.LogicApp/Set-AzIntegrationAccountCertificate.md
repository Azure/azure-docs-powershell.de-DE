---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 5b8da61caf8e3a89572f2054aea101a1ad8b70c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368442"
---
# <span data-ttu-id="1c5f7-101">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1c5f7-101">Set-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="1c5f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c5f7-102">SYNOPSIS</span></span>
<span data-ttu-id="1c5f7-103">Ändert das Zertifikat eines Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-103">Modifies an integration account certificate.</span></span>

## <span data-ttu-id="1c5f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c5f7-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1c5f7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c5f7-105">DESCRIPTION</span></span>
<span data-ttu-id="1c5f7-106">Das **Cmdlet Set-AzIntegrationAccountCertificate** ändert das Zertifikat eines Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-106">The **Set-AzIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="1c5f7-107">Dieses Cmdlet gibt ein Objekt zurück, das das Zertifikat des Integrationskontos darstellt.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="1c5f7-108">Angeben des Namens des Integrationskontos, des Ressourcengruppennamens und des Zertifikatnamens.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-108">Specifying the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="1c5f7-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1c5f7-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1c5f7-111">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1c5f7-112">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1c5f7-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1c5f7-113">EXAMPLES</span></span>

### <span data-ttu-id="1c5f7-114">Beispiel 1: Ändern eines Zertifikats für ein Integrationskonto</span><span class="sxs-lookup"><span data-stu-id="1c5f7-114">Example 1: Modify an integration account certificate</span></span>
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

<span data-ttu-id="1c5f7-115">Mit diesem Befehl wird das Zertifikat für das Integrationskonto in der angegebenen Ressourcengruppe geändert.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="1c5f7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c5f7-116">PARAMETERS</span></span>

### <span data-ttu-id="1c5f7-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="1c5f7-117">-CertificateName</span></span>
<span data-ttu-id="1c5f7-118">Gibt den Namen eines Zertifikats für ein Integrationskonto an.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="1c5f7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c5f7-119">-DefaultProfile</span></span>
<span data-ttu-id="1c5f7-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1c5f7-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c5f7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1c5f7-121">-Force</span></span>
<span data-ttu-id="1c5f7-122">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1c5f7-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1c5f7-123">-KeyName</span></span>
<span data-ttu-id="1c5f7-124">Gibt den Namen eines Zertifikatschlüssels im Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-124">Specifies the name of a certificate key in the key vault.</span></span>

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

### <span data-ttu-id="1c5f7-125">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="1c5f7-125">-KeyVaultId</span></span>
<span data-ttu-id="1c5f7-126">Gibt eine Schlüsseltresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-126">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="1c5f7-127">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="1c5f7-127">-KeyVersion</span></span>
<span data-ttu-id="1c5f7-128">Gibt die Version des Zertifikatschlüssels im Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-128">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="1c5f7-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="1c5f7-129">-Metadata</span></span>
<span data-ttu-id="1c5f7-130">Gibt ein Metadatenobjekt für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-130">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="1c5f7-131">-Name</span><span class="sxs-lookup"><span data-stu-id="1c5f7-131">-Name</span></span>
<span data-ttu-id="1c5f7-132">Gibt den Namen des Integrationskontos an.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-132">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="1c5f7-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="1c5f7-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="1c5f7-134">Gibt den Pfad einer öffentlichen Zertifikatdatei (CER) an.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-134">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="1c5f7-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c5f7-135">-ResourceGroupName</span></span>
<span data-ttu-id="1c5f7-136">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-136">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1c5f7-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c5f7-137">-Confirm</span></span>
<span data-ttu-id="1c5f7-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c5f7-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1c5f7-139">-WhatIf</span></span>
<span data-ttu-id="1c5f7-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c5f7-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c5f7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c5f7-142">CommonParameters</span></span>
<span data-ttu-id="1c5f7-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c5f7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c5f7-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c5f7-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c5f7-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1c5f7-145">INPUTS</span></span>

### <span data-ttu-id="1c5f7-146">System.String</span><span class="sxs-lookup"><span data-stu-id="1c5f7-146">System.String</span></span>

## <span data-ttu-id="1c5f7-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1c5f7-147">OUTPUTS</span></span>

### <span data-ttu-id="1c5f7-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1c5f7-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="1c5f7-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1c5f7-149">NOTES</span></span>

## <span data-ttu-id="1c5f7-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1c5f7-150">RELATED LINKS</span></span>

[<span data-ttu-id="1c5f7-151">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1c5f7-151">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="1c5f7-152">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1c5f7-152">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="1c5f7-153">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1c5f7-153">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)


