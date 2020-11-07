---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 1b2a3855703c1d91a17cfd164f6a65ce218da486
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652143"
---
# <span data-ttu-id="d2a9b-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="d2a9b-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="d2a9b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a9b-103">Ruft den Verschlüsselungsstatus des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="d2a9b-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="d2a9b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2a9b-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2a9b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2a9b-105">DESCRIPTION</span></span>
<span data-ttu-id="d2a9b-106">Das Cmdlet " **Get-AzVMDiskEncryptionStatus** " Ruft den Verschlüsselungsstatus des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="d2a9b-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="d2a9b-107">Sie zeigt den Verschlüsselungsstatus des Betriebssystems und der Datenmengen an.</span><span class="sxs-lookup"><span data-stu-id="d2a9b-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="d2a9b-108">Neben dem Verschlüsselungsstatus werden auch die URL für die Verschlüsselungs geheime URL, die URL für den Schlüssel Verschlüsselungsschlüssel, die Ressourcen-IDs der **keyvaults** angezeigt, in denen der Verschlüsselungsschlüssel und der Schlüssel Verschlüsselungsschlüssel für das Betriebssystemvolume vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d2a9b-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="d2a9b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2a9b-109">EXAMPLES</span></span>

### <span data-ttu-id="d2a9b-110">Beispiel 1: Abrufen des Verschlüsselungsstatus eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="d2a9b-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="d2a9b-111">Dieser Befehl ruft den Verschlüsselungsstatus des virtuellen Computers mit dem Namen VM001 ab.</span><span class="sxs-lookup"><span data-stu-id="d2a9b-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="d2a9b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2a9b-112">PARAMETERS</span></span>

### <span data-ttu-id="d2a9b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a9b-113">-DefaultProfile</span></span>
<span data-ttu-id="d2a9b-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d2a9b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2a9b-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="d2a9b-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="d2a9b-116">Der Name des Erweiterungs Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="d2a9b-116">The extension publisher name.</span></span> <span data-ttu-id="d2a9b-117">Geben Sie diesen Parameter nur an, um den Standardwert "Microsoft. Azure. Security" zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="d2a9b-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="d2a9b-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="d2a9b-118">-ExtensionType</span></span>
<span data-ttu-id="d2a9b-119">Der Erweiterungstyp.</span><span class="sxs-lookup"><span data-stu-id="d2a9b-119">The extension type.</span></span> <span data-ttu-id="d2a9b-120">Geben Sie diesen Parameter an, um den Standardwert "AzureDiskEncryption" für Windows-VMS und "AzureDiskEncryptionForLinux" für Linux-VMs zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="d2a9b-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="d2a9b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d2a9b-121">-Name</span></span>
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

### <span data-ttu-id="d2a9b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2a9b-122">-ResourceGroupName</span></span>
<span data-ttu-id="d2a9b-123">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="d2a9b-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d2a9b-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="d2a9b-124">-VMName</span></span>
<span data-ttu-id="d2a9b-125">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="d2a9b-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="d2a9b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a9b-126">CommonParameters</span></span>
<span data-ttu-id="d2a9b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2a9b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a9b-128">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2a9b-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a9b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2a9b-129">INPUTS</span></span>

### <span data-ttu-id="d2a9b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d2a9b-130">System.String</span></span>

## <span data-ttu-id="d2a9b-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2a9b-131">OUTPUTS</span></span>

### <span data-ttu-id="d2a9b-132">Microsoft. Azure. Commands. Compute. Extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="d2a9b-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="d2a9b-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2a9b-133">NOTES</span></span>

## <span data-ttu-id="d2a9b-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2a9b-134">RELATED LINKS</span></span>

[<span data-ttu-id="d2a9b-135">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="d2a9b-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="d2a9b-136">Satz-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="d2a9b-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


