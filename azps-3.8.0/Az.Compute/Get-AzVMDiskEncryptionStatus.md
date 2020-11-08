---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 4ad5ef08f9c12693a2fa4b4b372ee1320f90fb76
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005256"
---
# <span data-ttu-id="92fc7-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="92fc7-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="92fc7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92fc7-102">SYNOPSIS</span></span>
<span data-ttu-id="92fc7-103">Ruft den Verschlüsselungsstatus des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="92fc7-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="92fc7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="92fc7-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92fc7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92fc7-105">DESCRIPTION</span></span>
<span data-ttu-id="92fc7-106">Das Cmdlet " **Get-AzVMDiskEncryptionStatus** " Ruft den Verschlüsselungsstatus des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="92fc7-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="92fc7-107">Sie zeigt den Verschlüsselungsstatus des Betriebssystems und der Datenmengen an.</span><span class="sxs-lookup"><span data-stu-id="92fc7-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="92fc7-108">Neben dem Verschlüsselungsstatus werden auch die URL für die Verschlüsselungs geheime URL, die URL für den Schlüssel Verschlüsselungsschlüssel, die Ressourcen-IDs der **keyvaults** angezeigt, in denen der Verschlüsselungsschlüssel und der Schlüssel Verschlüsselungsschlüssel für das Betriebssystemvolume vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="92fc7-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="92fc7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92fc7-109">EXAMPLES</span></span>

### <span data-ttu-id="92fc7-110">Beispiel 1: Abrufen des Verschlüsselungsstatus eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="92fc7-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="92fc7-111">Dieser Befehl ruft den Verschlüsselungsstatus des virtuellen Computers mit dem Namen VM001 ab.</span><span class="sxs-lookup"><span data-stu-id="92fc7-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="92fc7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="92fc7-112">PARAMETERS</span></span>

### <span data-ttu-id="92fc7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92fc7-113">-DefaultProfile</span></span>
<span data-ttu-id="92fc7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="92fc7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92fc7-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="92fc7-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="92fc7-116">Der Name des Erweiterungs Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="92fc7-116">The extension publisher name.</span></span> <span data-ttu-id="92fc7-117">Geben Sie diesen Parameter nur an, um den Standardwert "Microsoft. Azure. Security" zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="92fc7-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="92fc7-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="92fc7-118">-ExtensionType</span></span>
<span data-ttu-id="92fc7-119">Der Erweiterungstyp.</span><span class="sxs-lookup"><span data-stu-id="92fc7-119">The extension type.</span></span> <span data-ttu-id="92fc7-120">Geben Sie diesen Parameter an, um den Standardwert "AzureDiskEncryption" für Windows-VMS und "AzureDiskEncryptionForLinux" für Linux-VMs zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="92fc7-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="92fc7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="92fc7-121">-Name</span></span>
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

### <span data-ttu-id="92fc7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92fc7-122">-ResourceGroupName</span></span>
<span data-ttu-id="92fc7-123">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="92fc7-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="92fc7-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="92fc7-124">-VMName</span></span>
<span data-ttu-id="92fc7-125">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="92fc7-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="92fc7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92fc7-126">CommonParameters</span></span>
<span data-ttu-id="92fc7-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92fc7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92fc7-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92fc7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92fc7-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92fc7-129">INPUTS</span></span>

### <span data-ttu-id="92fc7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="92fc7-130">System.String</span></span>

## <span data-ttu-id="92fc7-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92fc7-131">OUTPUTS</span></span>

### <span data-ttu-id="92fc7-132">Microsoft. Azure. Commands. Compute. Extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="92fc7-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="92fc7-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="92fc7-133">NOTES</span></span>

## <span data-ttu-id="92fc7-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92fc7-134">RELATED LINKS</span></span>

[<span data-ttu-id="92fc7-135">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="92fc7-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="92fc7-136">Satz-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="92fc7-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


