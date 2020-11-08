---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: cd61e2119ea84ccfc5fb6a7f5fe597e80c9fd417
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167124"
---
# <span data-ttu-id="35087-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="35087-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="35087-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35087-102">SYNOPSIS</span></span>
<span data-ttu-id="35087-103">Erstellt einen Azure-Verfügbarkeits Satz.</span><span class="sxs-lookup"><span data-stu-id="35087-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="35087-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35087-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-ProximityPlacementGroupId <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35087-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35087-105">DESCRIPTION</span></span>
<span data-ttu-id="35087-106">Mit dem Cmdlet **New-AzAvailabilitySet** wird ein Azure-Verfügbarkeits Satz erstellt.</span><span class="sxs-lookup"><span data-stu-id="35087-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="35087-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35087-107">EXAMPLES</span></span>

### <span data-ttu-id="35087-108">Beispiel 1: Erstellen eines Verfügbarkeits Satzes</span><span class="sxs-lookup"><span data-stu-id="35087-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="35087-109">Dieser Befehl erstellt einen Verfügbarkeits Satz mit dem Namen AvailabilitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="35087-109">This command creates an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="35087-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="35087-110">PARAMETERS</span></span>

### <span data-ttu-id="35087-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35087-111">-AsJob</span></span>
<span data-ttu-id="35087-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="35087-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35087-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35087-113">-DefaultProfile</span></span>
<span data-ttu-id="35087-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35087-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35087-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="35087-115">-Location</span></span>
<span data-ttu-id="35087-116">Gibt den Speicherort für den Verfügbarkeits Satz an.</span><span class="sxs-lookup"><span data-stu-id="35087-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="35087-117">-Name</span><span class="sxs-lookup"><span data-stu-id="35087-117">-Name</span></span>
<span data-ttu-id="35087-118">Gibt einen Namen für den Verfügbarkeits Satz an.</span><span class="sxs-lookup"><span data-stu-id="35087-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="35087-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="35087-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="35087-120">Gibt die Anzahl der Platt Formfehler-Domänen an.</span><span class="sxs-lookup"><span data-stu-id="35087-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="35087-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="35087-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="35087-122">Gibt die Anzahl der Platt Form Aktualisierungs Domänen an.</span><span class="sxs-lookup"><span data-stu-id="35087-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="35087-123">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="35087-123">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="35087-124">Die Ressourcen-ID der für diesen Verfügbarkeits Satz zu verwendenden Näherungs Platzierungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="35087-124">The resource id of the Proximity Placement Group to use with this availability set.</span></span>

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

### <span data-ttu-id="35087-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35087-125">-ResourceGroupName</span></span>
<span data-ttu-id="35087-126">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="35087-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="35087-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="35087-127">-Sku</span></span>
<span data-ttu-id="35087-128">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="35087-128">The Name of Sku.</span></span>
<span data-ttu-id="35087-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="35087-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="35087-130">Ausgerichtet: für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="35087-130">Aligned: For managed disks</span></span>
- <span data-ttu-id="35087-131">Klassisch: für nicht verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="35087-131">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="35087-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="35087-132">-Tag</span></span>
<span data-ttu-id="35087-133">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="35087-133">Key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35087-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35087-134">CommonParameters</span></span>
<span data-ttu-id="35087-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35087-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35087-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35087-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35087-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35087-137">INPUTS</span></span>

### <span data-ttu-id="35087-138">System. String</span><span class="sxs-lookup"><span data-stu-id="35087-138">System.String</span></span>

### <span data-ttu-id="35087-139">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="35087-139">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="35087-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35087-140">OUTPUTS</span></span>

### <span data-ttu-id="35087-141">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="35087-141">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="35087-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="35087-142">NOTES</span></span>

## <span data-ttu-id="35087-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35087-143">RELATED LINKS</span></span>

[<span data-ttu-id="35087-144">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="35087-144">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="35087-145">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="35087-145">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


