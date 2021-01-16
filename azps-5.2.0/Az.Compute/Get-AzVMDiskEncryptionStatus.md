---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 4ad5ef08f9c12693a2fa4b4b372ee1320f90fb76
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306392"
---
# <span data-ttu-id="8f1a7-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="8f1a7-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="8f1a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f1a7-102">SYNOPSIS</span></span>
<span data-ttu-id="8f1a7-103">Ruft den Verschlüsselungsstatus des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="8f1a7-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="8f1a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f1a7-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f1a7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f1a7-105">DESCRIPTION</span></span>
<span data-ttu-id="8f1a7-106">Das **Cmdlet "Get-AzVMDiskEncryptionStatus"** ruft den Verschlüsselungsstatus des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="8f1a7-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="8f1a7-107">Es zeigt den Verschlüsselungsstatus des Betriebssystems und datenvolumes an.</span><span class="sxs-lookup"><span data-stu-id="8f1a7-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="8f1a7-108">Zusätzlich zum Verschlüsselungsstatus werden auch die geheime Verschlüsselungs-URL, die Schlüsselverschlüsselungsschlüssel-URL, die Ressourcen-IDs der **KeyVaults** angezeigt, bei denen der Verschlüsselungsschlüssel und der Schlüsselverschlüsselungsschlüssel für das Betriebssystemvolume vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="8f1a7-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="8f1a7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8f1a7-109">EXAMPLES</span></span>

### <span data-ttu-id="8f1a7-110">Beispiel 1: Erhalten des Verschlüsselungsstatus eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="8f1a7-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="8f1a7-111">Dieser Befehl ruft den Verschlüsselungsstatus des virtuellen Computers "VM001" ab.</span><span class="sxs-lookup"><span data-stu-id="8f1a7-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="8f1a7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f1a7-112">PARAMETERS</span></span>

### <span data-ttu-id="8f1a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f1a7-113">-DefaultProfile</span></span>
<span data-ttu-id="8f1a7-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f1a7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f1a7-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="8f1a7-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="8f1a7-116">Der Herausgebername der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="8f1a7-116">The extension publisher name.</span></span> <span data-ttu-id="8f1a7-117">Geben Sie diesen Parameter nur an, um den Standardwert von "Microsoft.Azure.Security" zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="8f1a7-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="8f1a7-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="8f1a7-118">-ExtensionType</span></span>
<span data-ttu-id="8f1a7-119">Der Erweiterungstyp.</span><span class="sxs-lookup"><span data-stu-id="8f1a7-119">The extension type.</span></span> <span data-ttu-id="8f1a7-120">Geben Sie diesen Parameter an, um den Standardwert von "AzureDiskEncryption" für Windows-VMs und "AzureDiskEncryptionForLinux" für Linux-VMs außer Kraft zu setzen.</span><span class="sxs-lookup"><span data-stu-id="8f1a7-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="8f1a7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8f1a7-121">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f1a7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f1a7-122">-ResourceGroupName</span></span>
<span data-ttu-id="8f1a7-123">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="8f1a7-123">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f1a7-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="8f1a7-124">-VMName</span></span>
<span data-ttu-id="8f1a7-125">Gibt den Namen des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="8f1a7-125">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f1a7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f1a7-126">CommonParameters</span></span>
<span data-ttu-id="8f1a7-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f1a7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f1a7-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f1a7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f1a7-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8f1a7-129">INPUTS</span></span>

### <span data-ttu-id="8f1a7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8f1a7-130">System.String</span></span>

## <span data-ttu-id="8f1a7-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8f1a7-131">OUTPUTS</span></span>

### <span data-ttu-id="8f1a7-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="8f1a7-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="8f1a7-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8f1a7-133">NOTES</span></span>

## <span data-ttu-id="8f1a7-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8f1a7-134">RELATED LINKS</span></span>

[<span data-ttu-id="8f1a7-135">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="8f1a7-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="8f1a7-136">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="8f1a7-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


