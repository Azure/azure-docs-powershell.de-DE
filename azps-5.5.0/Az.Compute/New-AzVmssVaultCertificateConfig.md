---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5CC89899-00B6-424A-8896-FD32DE9DDA28
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssvaultcertificateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssVaultCertificateConfig.md
ms.openlocfilehash: 23b2b3acd5bb15771d3383cc39c6e0a69073a750
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144868"
---
# <span data-ttu-id="e7a39-101">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="e7a39-101">New-AzVmssVaultCertificateConfig</span></span>

## <span data-ttu-id="e7a39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7a39-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a39-103">Erstellt eine Zertifikatkonfiguration für den Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="e7a39-103">Creates a Key Vault certificate configuration.</span></span>

## <span data-ttu-id="e7a39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7a39-104">SYNTAX</span></span>

```
New-AzVmssVaultCertificateConfig [[-CertificateUrl] <String>] [[-CertificateStore] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7a39-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7a39-105">DESCRIPTION</span></span>
<span data-ttu-id="e7a39-106">Das **Cmdlet "New-AzVmssVaultCertificateConfig"** gibt das Geheime an, das auf virtuellen Computern des Virtual Machine Scale Set (VMSS) platziert werden muss.</span><span class="sxs-lookup"><span data-stu-id="e7a39-106">The **New-AzVmssVaultCertificateConfig** cmdlet specifies the secret that needs to be placed on the Virtual Machine Scale Set (VMSS) virtual machines.</span></span>
<span data-ttu-id="e7a39-107">Die Ausgabe dieses Cmdlets soll zusammen mit dem Add-AzVmssSecret verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7a39-107">The output of this cmdlet is intended to be used with the Add-AzVmssSecret cmdlet.</span></span>

## <span data-ttu-id="e7a39-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e7a39-108">EXAMPLES</span></span>

### <span data-ttu-id="e7a39-109">Beispiel 1: Erstellen einer Zertifikatkonfiguration für den Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="e7a39-109">Example 1: Create a Key Vault certificate configuration</span></span>
```
PS C:\> New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "MyCerts"
```

<span data-ttu-id="e7a39-110">Mit diesem Befehl wird eine Zertifikatkonfiguration für den Schlüsseltresor erstellt, die den Zertifikatspeicher "MyZertifikate" verwendet, der sich unter der angegebenen Zertifikat-URL befindet.</span><span class="sxs-lookup"><span data-stu-id="e7a39-110">This command creates a Key Vault certificate configuration that uses the certificate store named MyCerts located at the specified certificate URL.</span></span>

## <span data-ttu-id="e7a39-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7a39-111">PARAMETERS</span></span>

### <span data-ttu-id="e7a39-112">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="e7a39-112">-CertificateStore</span></span>
<span data-ttu-id="e7a39-113">Gibt den Zertifikatspeicher auf den virtuellen Computern in dem Skalierungssatz an, dem das Zertifikat hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e7a39-113">Specifies the certificate store on the virtual machines in the scale set where the certificate is added.</span></span>
<span data-ttu-id="e7a39-114">Dies ist nur für Skalierungssätze für Windows Virtual Machine gültig.</span><span class="sxs-lookup"><span data-stu-id="e7a39-114">This is only valid for Windows Virtual Machine Scale Sets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a39-115">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="e7a39-115">-CertificateUrl</span></span>
<span data-ttu-id="e7a39-116">Gibt den URI eines Zertifikats an, das im Schlüsseltresor gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="e7a39-116">Specifies the URI of a certificate stored in the Key Vault.</span></span>
<span data-ttu-id="e7a39-117">Dies ist die base64-Codierung des folgenden JSON-Objekts, das in UTF-8 codiert ist: { "data":" \<Base64-encoded-certificate\> ", "dataType":"pfx", "password":" \<pfx-file-password\> " }</span><span class="sxs-lookup"><span data-stu-id="e7a39-117">It is the base64 encoding of the following JSON Object which is encoded in UTF-8: { "data":"\<Base64-encoded-certificate\>", "dataType":"pfx", "password":"\<pfx-file-password\>" }</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a39-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a39-118">-DefaultProfile</span></span>
<span data-ttu-id="e7a39-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7a39-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7a39-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7a39-120">-Confirm</span></span>
<span data-ttu-id="e7a39-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7a39-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7a39-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e7a39-122">-WhatIf</span></span>
<span data-ttu-id="e7a39-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7a39-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7a39-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7a39-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7a39-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a39-125">CommonParameters</span></span>
<span data-ttu-id="e7a39-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7a39-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a39-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7a39-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a39-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e7a39-128">INPUTS</span></span>

### <span data-ttu-id="e7a39-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e7a39-129">System.String</span></span>

## <span data-ttu-id="e7a39-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e7a39-130">OUTPUTS</span></span>

### <span data-ttu-id="e7a39-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e7a39-131">Microsoft.Azure.Management.Compute.Models.VaultCertificate</span></span>

## <span data-ttu-id="e7a39-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e7a39-132">NOTES</span></span>

## <span data-ttu-id="e7a39-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e7a39-133">RELATED LINKS</span></span>

[<span data-ttu-id="e7a39-134">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="e7a39-134">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)
