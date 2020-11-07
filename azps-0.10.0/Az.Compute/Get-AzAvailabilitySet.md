---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: ef42e8910b9ff6a71277c998825aa53cd3ad085e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844672"
---
# <span data-ttu-id="2d292-101">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2d292-101">Get-AzAvailabilitySet</span></span>

## <span data-ttu-id="2d292-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d292-102">SYNOPSIS</span></span>
<span data-ttu-id="2d292-103">Ruft Azure-Verfügbarkeits Sätze in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="2d292-103">Gets Azure availability sets in a resource group.</span></span>

## <span data-ttu-id="2d292-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d292-104">SYNTAX</span></span>

```
Get-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d292-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d292-105">DESCRIPTION</span></span>
<span data-ttu-id="2d292-106">Das Cmdlet " **Get-AzAvailabilitySet** " ruft Azure-Verfügbarkeits Sätze in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="2d292-106">The **Get-AzAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="2d292-107">Sie können den Namen eines bestimmten verfügbaren Verfügbarkeits Satzes angeben, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d292-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="2d292-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d292-108">EXAMPLES</span></span>

### <span data-ttu-id="2d292-109">Beispiel 1: Abrufen eines bestimmten Verfügbarkeits Satzes</span><span class="sxs-lookup"><span data-stu-id="2d292-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="2d292-110">Dieser Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="2d292-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="2d292-111">Beispiel 2: Abrufen aller Verfügbarkeits Sätze</span><span class="sxs-lookup"><span data-stu-id="2d292-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="2d292-112">Dieser Befehl ruft alle Verfügbarkeits Sätze in der Ressourcengruppe mit dem Namen ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="2d292-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="2d292-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d292-113">PARAMETERS</span></span>

### <span data-ttu-id="2d292-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d292-114">-DefaultProfile</span></span>
<span data-ttu-id="2d292-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d292-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d292-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2d292-116">-Name</span></span>
<span data-ttu-id="2d292-117">Gibt den Namen eines Verfügbarkeits Satzes an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="2d292-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d292-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d292-118">-ResourceGroupName</span></span>
<span data-ttu-id="2d292-119">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2d292-119">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d292-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d292-120">CommonParameters</span></span>
<span data-ttu-id="2d292-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d292-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d292-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d292-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d292-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d292-123">INPUTS</span></span>

### <span data-ttu-id="2d292-124">Keine</span><span class="sxs-lookup"><span data-stu-id="2d292-124">None</span></span>
<span data-ttu-id="2d292-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2d292-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2d292-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d292-126">OUTPUTS</span></span>

### <span data-ttu-id="2d292-127">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2d292-127">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="2d292-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d292-128">NOTES</span></span>

## <span data-ttu-id="2d292-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d292-129">RELATED LINKS</span></span>

[<span data-ttu-id="2d292-130">Neu – AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2d292-130">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

[<span data-ttu-id="2d292-131">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2d292-131">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


