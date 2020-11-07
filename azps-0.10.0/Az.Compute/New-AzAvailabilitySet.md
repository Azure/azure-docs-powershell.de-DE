---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: 03e121493d8112116f5e8fc6ed492a54b67d47d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844516"
---
# <span data-ttu-id="255de-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="255de-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="255de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="255de-102">SYNOPSIS</span></span>
<span data-ttu-id="255de-103">Erstellt einen Azure-Verfügbarkeits Satz.</span><span class="sxs-lookup"><span data-stu-id="255de-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="255de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="255de-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="255de-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="255de-105">DESCRIPTION</span></span>
<span data-ttu-id="255de-106">Mit dem Cmdlet **New-AzAvailabilitySet** wird ein Azure-Verfügbarkeits Satz erstellt.</span><span class="sxs-lookup"><span data-stu-id="255de-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="255de-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="255de-107">EXAMPLES</span></span>

### <span data-ttu-id="255de-108">Beispiel 1: Erstellen eines Verfügbarkeits Satzes</span><span class="sxs-lookup"><span data-stu-id="255de-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="255de-109">Dieser Befehl erstellt einen Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="255de-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="255de-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="255de-110">PARAMETERS</span></span>

### <span data-ttu-id="255de-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="255de-111">-AsJob</span></span>
<span data-ttu-id="255de-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="255de-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="255de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="255de-113">-DefaultProfile</span></span>
<span data-ttu-id="255de-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="255de-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="255de-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="255de-115">-Location</span></span>
<span data-ttu-id="255de-116">Gibt den Speicherort für den Verfügbarkeits Satz an.</span><span class="sxs-lookup"><span data-stu-id="255de-116">Specifies the location for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255de-117">– Verwaltet</span><span class="sxs-lookup"><span data-stu-id="255de-117">-Managed</span></span>
<span data-ttu-id="255de-118">Verwalteter Verfügbarkeits Satz</span><span class="sxs-lookup"><span data-stu-id="255de-118">Managed Availability Set</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255de-119">-Name</span><span class="sxs-lookup"><span data-stu-id="255de-119">-Name</span></span>
<span data-ttu-id="255de-120">Gibt einen Namen für den Verfügbarkeits Satz an.</span><span class="sxs-lookup"><span data-stu-id="255de-120">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255de-121">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="255de-121">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="255de-122">Gibt die Anzahl der Platt Formfehler-Domänen an.</span><span class="sxs-lookup"><span data-stu-id="255de-122">Specifies the platform fault domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255de-123">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="255de-123">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="255de-124">Gibt die Anzahl der Platt Form Aktualisierungs Domänen an.</span><span class="sxs-lookup"><span data-stu-id="255de-124">Specifies the platform update domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255de-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="255de-125">-ResourceGroupName</span></span>
<span data-ttu-id="255de-126">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="255de-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="255de-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="255de-127">-Sku</span></span>
<span data-ttu-id="255de-128">Der Name der SKU</span><span class="sxs-lookup"><span data-stu-id="255de-128">The Name of Sku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="255de-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="255de-129">CommonParameters</span></span>
<span data-ttu-id="255de-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="255de-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="255de-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="255de-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="255de-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="255de-132">INPUTS</span></span>

### <span data-ttu-id="255de-133">Keine</span><span class="sxs-lookup"><span data-stu-id="255de-133">None</span></span>
<span data-ttu-id="255de-134">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="255de-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="255de-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="255de-135">OUTPUTS</span></span>

### <span data-ttu-id="255de-136">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="255de-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="255de-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="255de-137">NOTES</span></span>

## <span data-ttu-id="255de-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="255de-138">RELATED LINKS</span></span>

[<span data-ttu-id="255de-139">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="255de-139">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="255de-140">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="255de-140">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


