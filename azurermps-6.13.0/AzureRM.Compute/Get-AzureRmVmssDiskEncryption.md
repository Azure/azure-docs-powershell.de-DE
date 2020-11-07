---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssDiskEncryption.md
ms.openlocfilehash: 9b12daa0ab09bccb1620e7c976368e1dc0435ec9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664112"
---
# <span data-ttu-id="93989-101">Get-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="93989-101">Get-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="93989-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93989-102">SYNOPSIS</span></span>
<span data-ttu-id="93989-103">Zeigt den Datenträger Verschlüsselungsstatus eines VM-Skalierungs Satzes an.</span><span class="sxs-lookup"><span data-stu-id="93989-103">Shows the disk encryption status of a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93989-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93989-104">SYNTAX</span></span>

```
Get-AzureRmVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93989-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93989-105">DESCRIPTION</span></span>
<span data-ttu-id="93989-106">Zeigt den Datenträger Verschlüsselungsstatus eines VM-Skalierungs Satzes an.</span><span class="sxs-lookup"><span data-stu-id="93989-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="93989-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93989-107">EXAMPLES</span></span>

### <span data-ttu-id="93989-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="93989-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="93989-109">Zeigt den Datenträger Verschlüsselungsstatus des VM-Skalierungs Satzes mit dem Namen "VMSS001" an, der zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="93989-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="93989-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="93989-110">PARAMETERS</span></span>

### <span data-ttu-id="93989-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93989-111">-DefaultProfile</span></span>
<span data-ttu-id="93989-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93989-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93989-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="93989-113">-ExtensionName</span></span>
<span data-ttu-id="93989-114">Der Name der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="93989-114">The extension name.</span></span>
<span data-ttu-id="93989-115">Wenn dieser Parameter nicht angegeben ist, werden die Standardwerte AzureDiskEncryption für Windows VMS und AzureDiskEncryptionForLinux für Linux VMs verwendet.</span><span class="sxs-lookup"><span data-stu-id="93989-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93989-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93989-116">-ResourceGroupName</span></span>
<span data-ttu-id="93989-117">Ressourcengruppenname des Skalierungs Satzes für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="93989-117">Resource group name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="93989-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="93989-118">-VMScaleSetName</span></span>
<span data-ttu-id="93989-119">Der Skalierungs Satz Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="93989-119">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93989-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93989-120">CommonParameters</span></span>
<span data-ttu-id="93989-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93989-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93989-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93989-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93989-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93989-123">INPUTS</span></span>

### <span data-ttu-id="93989-124">System. String</span><span class="sxs-lookup"><span data-stu-id="93989-124">System.String</span></span>

## <span data-ttu-id="93989-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93989-125">OUTPUTS</span></span>

### <span data-ttu-id="93989-126">Microsoft. Azure. Commands. Compute. Models. PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="93989-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="93989-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="93989-127">NOTES</span></span>

## <span data-ttu-id="93989-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93989-128">RELATED LINKS</span></span>
