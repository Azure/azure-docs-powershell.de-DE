---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: 2e3fc51410ff5a6fa9fca2aaeec0fe326012a8bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505629"
---
# <span data-ttu-id="05e9e-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="05e9e-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="05e9e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="05e9e-103">Erstellt einen Azure-Verfügbarkeits Satz.</span><span class="sxs-lookup"><span data-stu-id="05e9e-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05e9e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05e9e-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05e9e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05e9e-105">DESCRIPTION</span></span>
<span data-ttu-id="05e9e-106">Mit dem Cmdlet **New-AzureRmAvailabilitySet** wird ein Azure-Verfügbarkeits Satz erstellt.</span><span class="sxs-lookup"><span data-stu-id="05e9e-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="05e9e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05e9e-107">EXAMPLES</span></span>

### <span data-ttu-id="05e9e-108">Beispiel 1: Erstellen eines Verfügbarkeits Satzes</span><span class="sxs-lookup"><span data-stu-id="05e9e-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="05e9e-109">Dieser Befehl erstellt einen Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="05e9e-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="05e9e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="05e9e-110">PARAMETERS</span></span>

### <span data-ttu-id="05e9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05e9e-111">-DefaultProfile</span></span>
<span data-ttu-id="05e9e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="05e9e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05e9e-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="05e9e-113">-Location</span></span>
<span data-ttu-id="05e9e-114">Gibt den Speicherort für den Verfügbarkeits Satz an.</span><span class="sxs-lookup"><span data-stu-id="05e9e-114">Specifies the location for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05e9e-115">– Verwaltet</span><span class="sxs-lookup"><span data-stu-id="05e9e-115">-Managed</span></span>
<span data-ttu-id="05e9e-116">Verwalteter Verfügbarkeits Satz</span><span class="sxs-lookup"><span data-stu-id="05e9e-116">Managed Availability Set</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05e9e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="05e9e-117">-Name</span></span>
<span data-ttu-id="05e9e-118">Gibt einen Namen für den Verfügbarkeits Satz an.</span><span class="sxs-lookup"><span data-stu-id="05e9e-118">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05e9e-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="05e9e-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="05e9e-120">Gibt die Anzahl der Platt Formfehler-Domänen an.</span><span class="sxs-lookup"><span data-stu-id="05e9e-120">Specifies the platform fault domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05e9e-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="05e9e-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="05e9e-122">Gibt die Anzahl der Platt Form Aktualisierungs Domänen an.</span><span class="sxs-lookup"><span data-stu-id="05e9e-122">Specifies the platform update domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05e9e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05e9e-123">-ResourceGroupName</span></span>
<span data-ttu-id="05e9e-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="05e9e-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="05e9e-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="05e9e-125">-Sku</span></span>
<span data-ttu-id="05e9e-126">Der Name der SKU</span><span class="sxs-lookup"><span data-stu-id="05e9e-126">The Name of Sku</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05e9e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05e9e-127">CommonParameters</span></span>
<span data-ttu-id="05e9e-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05e9e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05e9e-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05e9e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05e9e-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05e9e-130">INPUTS</span></span>

## <span data-ttu-id="05e9e-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05e9e-131">OUTPUTS</span></span>

## <span data-ttu-id="05e9e-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="05e9e-132">NOTES</span></span>

## <span data-ttu-id="05e9e-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05e9e-133">RELATED LINKS</span></span>

[<span data-ttu-id="05e9e-134">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="05e9e-134">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="05e9e-135">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="05e9e-135">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


