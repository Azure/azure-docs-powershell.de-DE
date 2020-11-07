---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzSnapshot.md
ms.openlocfilehash: 25395cca287e7f711d5e124ab12919a0b5c01ce4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844659"
---
# <span data-ttu-id="086c9-101">Get-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="086c9-101">Get-AzSnapshot</span></span>

## <span data-ttu-id="086c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="086c9-102">SYNOPSIS</span></span>
<span data-ttu-id="086c9-103">Ruft die Eigenschaften eines Snapshots ab.</span><span class="sxs-lookup"><span data-stu-id="086c9-103">Gets the properties of a snapshot</span></span>

## <span data-ttu-id="086c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="086c9-104">SYNTAX</span></span>

```
Get-AzSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="086c9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="086c9-105">DESCRIPTION</span></span>
<span data-ttu-id="086c9-106">Das Cmdlet " **Get-AzSnapshot** " Ruft die Eigenschaften eines Snapshots ab.</span><span class="sxs-lookup"><span data-stu-id="086c9-106">The **Get-AzSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="086c9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="086c9-107">EXAMPLES</span></span>

### <span data-ttu-id="086c9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="086c9-108">Example 1</span></span>
```
PS C:\> Get-AzSnapshot
```

<span data-ttu-id="086c9-109">Dieser Befehl ruft die Eigenschaften aller Snapshots des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="086c9-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="086c9-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="086c9-110">Example 2</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="086c9-111">Dieser Befehl ruft die Eigenschaften aller Schnappschüsse in der Ressourcengruppe mit dem Namen "ResourceGroupName1" ab.</span><span class="sxs-lookup"><span data-stu-id="086c9-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="086c9-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="086c9-112">Example 3</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="086c9-113">Mit diesem Befehl werden die Eigenschaften des Snapshots mit dem Namen "SnapshotName1" in der Ressourcengruppe "ResourceGroupName1" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="086c9-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="086c9-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="086c9-114">PARAMETERS</span></span>

### <span data-ttu-id="086c9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="086c9-115">-DefaultProfile</span></span>
<span data-ttu-id="086c9-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="086c9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="086c9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="086c9-117">-ResourceGroupName</span></span>
<span data-ttu-id="086c9-118">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="086c9-118">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="086c9-119">-Snapshotname</span><span class="sxs-lookup"><span data-stu-id="086c9-119">-SnapshotName</span></span>
<span data-ttu-id="086c9-120">Gibt den Namen eines Schnappschusses an.</span><span class="sxs-lookup"><span data-stu-id="086c9-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="086c9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="086c9-121">CommonParameters</span></span>
<span data-ttu-id="086c9-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="086c9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="086c9-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="086c9-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="086c9-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="086c9-124">INPUTS</span></span>

### <span data-ttu-id="086c9-125">System. String</span><span class="sxs-lookup"><span data-stu-id="086c9-125">System.String</span></span>

## <span data-ttu-id="086c9-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="086c9-126">OUTPUTS</span></span>

### <span data-ttu-id="086c9-127">Microsoft. Azure. Commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="086c9-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="086c9-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="086c9-128">NOTES</span></span>

## <span data-ttu-id="086c9-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="086c9-129">RELATED LINKS</span></span>

