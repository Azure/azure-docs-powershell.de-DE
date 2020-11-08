---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
ms.openlocfilehash: 298d6bac6b2c1b37cff47a22a1647caafdb3e843
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166418"
---
# <span data-ttu-id="d1eb9-101">Restore-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d1eb9-101">Restore-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="d1eb9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="d1eb9-103">Stellt ein Zertifikat aus einer Sicherungsdatei in einem schlüsseltresor wieder her.</span><span class="sxs-lookup"><span data-stu-id="d1eb9-103">Restores a certificate in a key vault from a backup file.</span></span>

## <span data-ttu-id="d1eb9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1eb9-104">SYNTAX</span></span>

### <span data-ttu-id="d1eb9-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1eb9-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1eb9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d1eb9-106">ByInputObject</span></span>
```
Restore-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1eb9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d1eb9-107">ByResourceId</span></span>
```
Restore-AzKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1eb9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1eb9-108">DESCRIPTION</span></span>
<span data-ttu-id="d1eb9-109">Mit dem Cmdlet **Restore-AzKeyVaultCertificate** wird ein Zertifikat im angegebenen schlüsseltresor aus einer Sicherungsdatei erstellt.</span><span class="sxs-lookup"><span data-stu-id="d1eb9-109">The **Restore-AzKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="d1eb9-110">Dieses Zertifikat ist ein Replikat des gesicherten Zertifikats in der Eingabedatei und hat denselben Namen wie das ursprüngliche Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="d1eb9-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="d1eb9-111">Wenn der schlüsseltresor bereits ein Zertifikat mit demselben Namen enthält, schlägt dieses Cmdlet fehl, anstatt das ursprüngliche Zertifikat zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="d1eb9-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="d1eb9-112">Wenn die Sicherung mehrere Versionen eines Zertifikats enthält, werden alle Versionen wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="d1eb9-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="d1eb9-113">Der schlüsseltresor, in den Sie das Zertifikat wiederherstellen, kann sich vom schlüsseltresor unterscheiden, von dem Sie das Zertifikat gesichert haben.</span><span class="sxs-lookup"><span data-stu-id="d1eb9-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="d1eb9-114">Der schlüsseltresor muss jedoch dasselbe Abonnement verwenden und sich in einem Azure-Bereich in derselben geografischen Region befinden (beispielsweise in Nordamerika).</span><span class="sxs-lookup"><span data-stu-id="d1eb9-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="d1eb9-115">Informationen finden Sie im Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) für die Zuordnung von Azure-Regionen zu Geographien.</span><span class="sxs-lookup"><span data-stu-id="d1eb9-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="d1eb9-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1eb9-116">EXAMPLES</span></span>

### <span data-ttu-id="d1eb9-117">Beispiel 1: Wiederherstellen eines gesicherten Zertifikats</span><span class="sxs-lookup"><span data-stu-id="d1eb9-117">Example 1: Restore a backed-up certificate</span></span>
```powershell
PS C:\> Restore-AzKeyVaultCertificate -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/25/2018 3:47:41 AM

                [Not After]
                  11/25/2018 2:57:41 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Purgeable
Enabled       : True
Expires       : 11/25/2018 10:57:41 AM
NotBefore     : 5/25/2018 10:47:41 AM
Created       : 5/25/2018 10:57:41 AM
Updated       : 5/25/2018 10:57:41 AM
Tags          : 
VaultName     : MyKeyVault
Name          : cert1
Version       : bd406f6d6b3a41a1a1c633494d8c3c3a
Id            : https://mykeyvault.vault.azure.net:443/certificates/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
```

<span data-ttu-id="d1eb9-118">Mit diesem Befehl wird ein Zertifikat, einschließlich aller Versionen, aus der Sicherungsdatei mit dem Namen Backup. BLOB in den schlüsseltresor mit dem Namen MyKeyVault wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="d1eb9-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="d1eb9-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1eb9-119">PARAMETERS</span></span>

### <span data-ttu-id="d1eb9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1eb9-120">-DefaultProfile</span></span>
<span data-ttu-id="d1eb9-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d1eb9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1eb9-122">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="d1eb9-122">-InputFile</span></span>
<span data-ttu-id="d1eb9-123">Eingabedatei.</span><span class="sxs-lookup"><span data-stu-id="d1eb9-123">Input file.</span></span>
<span data-ttu-id="d1eb9-124">Die Eingabedatei mit dem gesicherten BLOB</span><span class="sxs-lookup"><span data-stu-id="d1eb9-124">The input file containing the backed-up blob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1eb9-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d1eb9-125">-InputObject</span></span>
<span data-ttu-id="d1eb9-126">Keyvault-Objekt</span><span class="sxs-lookup"><span data-stu-id="d1eb9-126">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1eb9-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d1eb9-127">-ResourceId</span></span>
<span data-ttu-id="d1eb9-128">Keyvault-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="d1eb9-128">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1eb9-129">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="d1eb9-129">-VaultName</span></span>
<span data-ttu-id="d1eb9-130">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="d1eb9-130">Vault name.</span></span>
<span data-ttu-id="d1eb9-131">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="d1eb9-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1eb9-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d1eb9-132">-Confirm</span></span>
<span data-ttu-id="d1eb9-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1eb9-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1eb9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1eb9-134">-WhatIf</span></span>
<span data-ttu-id="d1eb9-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1eb9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1eb9-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1eb9-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1eb9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1eb9-137">CommonParameters</span></span>
<span data-ttu-id="d1eb9-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1eb9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1eb9-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1eb9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1eb9-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1eb9-140">INPUTS</span></span>

### <span data-ttu-id="d1eb9-141">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d1eb9-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="d1eb9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d1eb9-142">System.String</span></span>

## <span data-ttu-id="d1eb9-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1eb9-143">OUTPUTS</span></span>

### <span data-ttu-id="d1eb9-144">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="d1eb9-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="d1eb9-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1eb9-145">NOTES</span></span>

## <span data-ttu-id="d1eb9-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1eb9-146">RELATED LINKS</span></span>
