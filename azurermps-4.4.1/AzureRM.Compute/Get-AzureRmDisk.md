---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e598c266f46815e7005c43e2d354ad8ece06efc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504217"
---
# <span data-ttu-id="0de8e-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="0de8e-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="0de8e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0de8e-102">SYNOPSIS</span></span>
<span data-ttu-id="0de8e-103">Ruft die Eigenschaften eines Datenträgers ab.</span><span class="sxs-lookup"><span data-stu-id="0de8e-103">Gets the properties of a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0de8e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0de8e-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0de8e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0de8e-105">DESCRIPTION</span></span>
<span data-ttu-id="0de8e-106">Das Cmdlet " **Get-AzureRmDisk** " Ruft die Eigenschaften eines Datenträgers ab.</span><span class="sxs-lookup"><span data-stu-id="0de8e-106">The **Get-AzureRmDisk** cmdlet gets the properties of a disk.</span></span>

## <span data-ttu-id="0de8e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0de8e-107">EXAMPLES</span></span>

### <span data-ttu-id="0de8e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0de8e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="0de8e-109">Dieser Befehl ruft die Eigenschaften des Datenträgers mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="0de8e-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="0de8e-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0de8e-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="0de8e-111">Dieser Befehl ruft die Eigenschaften aller Datenträger in der Ressourcengruppe "ResourceGroup01" ab.</span><span class="sxs-lookup"><span data-stu-id="0de8e-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="0de8e-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0de8e-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="0de8e-113">Mit diesem Befehl werden die Eigenschaften aller Datenträger unter dem Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0de8e-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="0de8e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0de8e-114">PARAMETERS</span></span>

### <span data-ttu-id="0de8e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0de8e-115">-DefaultProfile</span></span>
<span data-ttu-id="0de8e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0de8e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0de8e-117">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="0de8e-117">-DiskName</span></span>
<span data-ttu-id="0de8e-118">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="0de8e-118">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0de8e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0de8e-119">-ResourceGroupName</span></span>
<span data-ttu-id="0de8e-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0de8e-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0de8e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0de8e-121">CommonParameters</span></span>
<span data-ttu-id="0de8e-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0de8e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0de8e-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0de8e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0de8e-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0de8e-124">INPUTS</span></span>

### <span data-ttu-id="0de8e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0de8e-125">System.String</span></span>

## <span data-ttu-id="0de8e-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0de8e-126">OUTPUTS</span></span>

### <span data-ttu-id="0de8e-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="0de8e-127">System.Object</span></span>

## <span data-ttu-id="0de8e-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="0de8e-128">NOTES</span></span>

## <span data-ttu-id="0de8e-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0de8e-129">RELATED LINKS</span></span>

