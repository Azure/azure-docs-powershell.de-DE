---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: 5a1d583d9eee535f519b6748867b4026dcc45006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664363"
---
# <span data-ttu-id="25165-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="25165-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="25165-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25165-102">SYNOPSIS</span></span>
<span data-ttu-id="25165-103">Erstellt einen Azure-Verfügbarkeits Satz.</span><span class="sxs-lookup"><span data-stu-id="25165-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25165-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25165-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25165-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25165-105">DESCRIPTION</span></span>
<span data-ttu-id="25165-106">Mit dem Cmdlet **New-AzureRmAvailabilitySet** wird ein Azure-Verfügbarkeits Satz erstellt.</span><span class="sxs-lookup"><span data-stu-id="25165-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="25165-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25165-107">EXAMPLES</span></span>

### <span data-ttu-id="25165-108">Beispiel 1: Erstellen eines Verfügbarkeits Satzes</span><span class="sxs-lookup"><span data-stu-id="25165-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="25165-109">Dieser Befehl erstellt einen Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="25165-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="25165-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="25165-110">PARAMETERS</span></span>

### <span data-ttu-id="25165-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25165-111">-AsJob</span></span>
<span data-ttu-id="25165-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="25165-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="25165-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25165-113">-DefaultProfile</span></span>
<span data-ttu-id="25165-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25165-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25165-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="25165-115">-Location</span></span>
<span data-ttu-id="25165-116">Gibt den Speicherort für den Verfügbarkeits Satz an.</span><span class="sxs-lookup"><span data-stu-id="25165-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="25165-117">-Name</span><span class="sxs-lookup"><span data-stu-id="25165-117">-Name</span></span>
<span data-ttu-id="25165-118">Gibt einen Namen für den Verfügbarkeits Satz an.</span><span class="sxs-lookup"><span data-stu-id="25165-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="25165-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="25165-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="25165-120">Gibt die Anzahl der Platt Formfehler-Domänen an.</span><span class="sxs-lookup"><span data-stu-id="25165-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="25165-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="25165-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="25165-122">Gibt die Anzahl der Platt Form Aktualisierungs Domänen an.</span><span class="sxs-lookup"><span data-stu-id="25165-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="25165-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25165-123">-ResourceGroupName</span></span>
<span data-ttu-id="25165-124">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="25165-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="25165-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="25165-125">-Sku</span></span>
<span data-ttu-id="25165-126">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="25165-126">The Name of Sku.</span></span>
<span data-ttu-id="25165-127">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="25165-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="25165-128">Ausgerichtet: für verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="25165-128">Aligned: For managed disks</span></span>
- <span data-ttu-id="25165-129">Klassisch: für nicht verwaltete Datenträger</span><span class="sxs-lookup"><span data-stu-id="25165-129">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="25165-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="25165-130">-Tag</span></span>
<span data-ttu-id="25165-131">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="25165-131">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="25165-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25165-132">CommonParameters</span></span>
<span data-ttu-id="25165-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25165-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25165-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25165-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25165-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25165-135">INPUTS</span></span>

### <span data-ttu-id="25165-136">System. String</span><span class="sxs-lookup"><span data-stu-id="25165-136">System.String</span></span>

### <span data-ttu-id="25165-137">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="25165-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="25165-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25165-138">OUTPUTS</span></span>

### <span data-ttu-id="25165-139">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="25165-139">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="25165-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="25165-140">NOTES</span></span>

## <span data-ttu-id="25165-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25165-141">RELATED LINKS</span></span>

[<span data-ttu-id="25165-142">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="25165-142">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="25165-143">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="25165-143">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


