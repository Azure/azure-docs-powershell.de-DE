---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
ms.openlocfilehash: 0d7312d7ecbddf15530438e9729e470bd202e488
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663606"
---
# <span data-ttu-id="3d466-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="3d466-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="3d466-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d466-102">SYNOPSIS</span></span>
<span data-ttu-id="3d466-103">Ruft den Verschlüsselungsstatus des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="3d466-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d466-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d466-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d466-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d466-105">DESCRIPTION</span></span>
<span data-ttu-id="3d466-106">Das Cmdlet " **Get-AzureRmVMDiskEncryptionStatus** " Ruft den Verschlüsselungsstatus des virtuellen Computers ab.</span><span class="sxs-lookup"><span data-stu-id="3d466-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="3d466-107">Sie zeigt den Verschlüsselungsstatus des Betriebssystems und der Datenmengen an.</span><span class="sxs-lookup"><span data-stu-id="3d466-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="3d466-108">Neben dem Verschlüsselungsstatus werden auch die URL für die Verschlüsselungs geheime URL, die URL für den Schlüssel Verschlüsselungsschlüssel, die Ressourcen-IDs der **keyvaults** angezeigt, in denen der Verschlüsselungsschlüssel und der Schlüssel Verschlüsselungsschlüssel für das Betriebssystemvolume vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3d466-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="3d466-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d466-109">EXAMPLES</span></span>

### <span data-ttu-id="3d466-110">Beispiel 1: Abrufen des Verschlüsselungsstatus eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="3d466-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="3d466-111">Dieser Befehl ruft den Verschlüsselungsstatus des virtuellen Computers mit dem Namen VM001 ab.</span><span class="sxs-lookup"><span data-stu-id="3d466-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="3d466-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d466-112">PARAMETERS</span></span>

### <span data-ttu-id="3d466-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d466-113">-DefaultProfile</span></span>
<span data-ttu-id="3d466-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3d466-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d466-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3d466-115">-Name</span></span>
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

### <span data-ttu-id="3d466-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d466-116">-ResourceGroupName</span></span>
<span data-ttu-id="3d466-117">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="3d466-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3d466-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="3d466-118">-VMName</span></span>
<span data-ttu-id="3d466-119">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="3d466-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="3d466-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d466-120">CommonParameters</span></span>
<span data-ttu-id="3d466-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d466-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d466-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d466-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d466-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d466-123">INPUTS</span></span>

## <span data-ttu-id="3d466-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d466-124">OUTPUTS</span></span>

## <span data-ttu-id="3d466-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d466-125">NOTES</span></span>

## <span data-ttu-id="3d466-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d466-126">RELATED LINKS</span></span>

[<span data-ttu-id="3d466-127">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="3d466-127">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="3d466-128">Satz-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="3d466-128">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


