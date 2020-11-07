---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: ef00a9e425f67fbfc1ce47746503b574d483598f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848539"
---
# <span data-ttu-id="8499e-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8499e-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="8499e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8499e-102">SYNOPSIS</span></span>
<span data-ttu-id="8499e-103">Ruft Azure-Verfügbarkeits Sätze in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="8499e-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8499e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8499e-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8499e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8499e-105">DESCRIPTION</span></span>
<span data-ttu-id="8499e-106">Das Cmdlet " **Get-AzureRmAvailabilitySet** " ruft Azure-Verfügbarkeits Sätze in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="8499e-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="8499e-107">Sie können den Namen eines bestimmten verfügbaren Verfügbarkeits Satzes angeben, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8499e-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="8499e-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8499e-108">EXAMPLES</span></span>

### <span data-ttu-id="8499e-109">Beispiel 1: Abrufen eines bestimmten Verfügbarkeits Satzes</span><span class="sxs-lookup"><span data-stu-id="8499e-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="8499e-110">Dieser Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="8499e-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="8499e-111">Beispiel 2: Abrufen aller Verfügbarkeits Sätze</span><span class="sxs-lookup"><span data-stu-id="8499e-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="8499e-112">Dieser Befehl ruft alle Verfügbarkeits Sätze in der Ressourcengruppe mit dem Namen ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="8499e-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="8499e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8499e-113">PARAMETERS</span></span>

### <span data-ttu-id="8499e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8499e-114">-DefaultProfile</span></span>
<span data-ttu-id="8499e-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8499e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8499e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8499e-116">-Name</span></span>
<span data-ttu-id="8499e-117">Gibt den Namen eines Verfügbarkeits Satzes an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="8499e-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8499e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8499e-118">-ResourceGroupName</span></span>
<span data-ttu-id="8499e-119">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8499e-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8499e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8499e-120">CommonParameters</span></span>
<span data-ttu-id="8499e-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8499e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8499e-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8499e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8499e-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8499e-123">INPUTS</span></span>

### <span data-ttu-id="8499e-124">Keine</span><span class="sxs-lookup"><span data-stu-id="8499e-124">None</span></span>
<span data-ttu-id="8499e-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8499e-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8499e-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8499e-126">OUTPUTS</span></span>

### <span data-ttu-id="8499e-127">Microsoft. Azure. Commands. Compute. Models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8499e-127">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="8499e-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="8499e-128">NOTES</span></span>

## <span data-ttu-id="8499e-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8499e-129">RELATED LINKS</span></span>

[<span data-ttu-id="8499e-130">Neu – AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8499e-130">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="8499e-131">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8499e-131">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


