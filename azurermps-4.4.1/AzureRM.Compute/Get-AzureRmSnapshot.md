---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 98297d46416b23cd127e5ab5b65ce2fcfac38aa0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479906"
---
# <span data-ttu-id="3848b-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="3848b-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="3848b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3848b-102">SYNOPSIS</span></span>
<span data-ttu-id="3848b-103">Ruft die Eigenschaften eines Snapshots ab.</span><span class="sxs-lookup"><span data-stu-id="3848b-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3848b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3848b-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3848b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3848b-105">DESCRIPTION</span></span>
<span data-ttu-id="3848b-106">Das Cmdlet " **Get-AzureRmSnapshot** " Ruft die Eigenschaften eines Snapshots ab.</span><span class="sxs-lookup"><span data-stu-id="3848b-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="3848b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3848b-107">EXAMPLES</span></span>

### <span data-ttu-id="3848b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3848b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="3848b-109">Dieser Befehl ruft die Eigenschaften aller Snapshots des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="3848b-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="3848b-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3848b-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="3848b-111">Dieser Befehl ruft die Eigenschaften aller Schnappschüsse in der Ressourcengruppe mit dem Namen "ResourceGroupName1" ab.</span><span class="sxs-lookup"><span data-stu-id="3848b-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="3848b-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3848b-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="3848b-113">Mit diesem Befehl werden die Eigenschaften des Snapshots mit dem Namen "SnapshotName1" in der Ressourcengruppe "ResourceGroupName1" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3848b-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="3848b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3848b-114">PARAMETERS</span></span>

### <span data-ttu-id="3848b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3848b-115">-DefaultProfile</span></span>
<span data-ttu-id="3848b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3848b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3848b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3848b-117">-ResourceGroupName</span></span>
<span data-ttu-id="3848b-118">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3848b-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3848b-119">-Snapshotname</span><span class="sxs-lookup"><span data-stu-id="3848b-119">-SnapshotName</span></span>
<span data-ttu-id="3848b-120">Gibt den Namen eines Schnappschusses an.</span><span class="sxs-lookup"><span data-stu-id="3848b-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="3848b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3848b-121">CommonParameters</span></span>
<span data-ttu-id="3848b-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3848b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3848b-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3848b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3848b-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3848b-124">INPUTS</span></span>

### <span data-ttu-id="3848b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3848b-125">System.String</span></span>

## <span data-ttu-id="3848b-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3848b-126">OUTPUTS</span></span>

### <span data-ttu-id="3848b-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="3848b-127">System.Object</span></span>

## <span data-ttu-id="3848b-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="3848b-128">NOTES</span></span>

## <span data-ttu-id="3848b-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3848b-129">RELATED LINKS</span></span>

