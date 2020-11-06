---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
ms.openlocfilehash: 769cb913c04c435071c6b743f0d3de533128986f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504225"
---
# <span data-ttu-id="10de3-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="10de3-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="10de3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="10de3-102">SYNOPSIS</span></span>
<span data-ttu-id="10de3-103">Ruft Azure-Verfügbarkeits Sätze in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="10de3-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10de3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="10de3-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10de3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10de3-105">DESCRIPTION</span></span>
<span data-ttu-id="10de3-106">Das Cmdlet " **Get-AzureRmAvailabilitySet** " ruft Azure-Verfügbarkeits Sätze in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="10de3-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="10de3-107">Sie können den Namen eines bestimmten verfügbaren Verfügbarkeits Satzes angeben, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="10de3-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="10de3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="10de3-108">EXAMPLES</span></span>

### <span data-ttu-id="10de3-109">Beispiel 1: Abrufen eines bestimmten Verfügbarkeits Satzes</span><span class="sxs-lookup"><span data-stu-id="10de3-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="10de3-110">Dieser Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="10de3-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="10de3-111">Beispiel 2: Abrufen aller Verfügbarkeits Sätze</span><span class="sxs-lookup"><span data-stu-id="10de3-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="10de3-112">Dieser Befehl ruft alle Verfügbarkeits Sätze in der Ressourcengruppe mit dem Namen ResourceGroup11 ab.</span><span class="sxs-lookup"><span data-stu-id="10de3-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="10de3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="10de3-113">PARAMETERS</span></span>

### <span data-ttu-id="10de3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10de3-114">-DefaultProfile</span></span>
<span data-ttu-id="10de3-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="10de3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10de3-116">-Name</span><span class="sxs-lookup"><span data-stu-id="10de3-116">-Name</span></span>
<span data-ttu-id="10de3-117">Gibt den Namen eines Verfügbarkeits Satzes an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="10de3-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10de3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10de3-118">-ResourceGroupName</span></span>
<span data-ttu-id="10de3-119">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="10de3-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="10de3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10de3-120">CommonParameters</span></span>
<span data-ttu-id="10de3-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10de3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10de3-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10de3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10de3-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="10de3-123">INPUTS</span></span>

## <span data-ttu-id="10de3-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="10de3-124">OUTPUTS</span></span>

## <span data-ttu-id="10de3-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="10de3-125">NOTES</span></span>

## <span data-ttu-id="10de3-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="10de3-126">RELATED LINKS</span></span>

[<span data-ttu-id="10de3-127">Neu – AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="10de3-127">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="10de3-128">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="10de3-128">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


