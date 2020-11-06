---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 18f492147e897b8061795434c309cc63729bec5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481157"
---
# <span data-ttu-id="41161-101">Get-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="41161-101">Get-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="41161-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="41161-102">SYNOPSIS</span></span>
<span data-ttu-id="41161-103">Ruft das Konto ab.</span><span class="sxs-lookup"><span data-stu-id="41161-103">Gets the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41161-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="41161-104">SYNTAX</span></span>

### <span data-ttu-id="41161-105">ResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="41161-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccount [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41161-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="41161-106">AccountNameParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41161-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41161-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="41161-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41161-108">DESCRIPTION</span></span>
<span data-ttu-id="41161-109">Das Cmdlet " **Get-AzureRmLocationBasedServicesAccount** " Ruft ein bereitgestelltes standortbasiertes Dienstkonto ab, entweder nach Ressourcengruppe und Name oder nach Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="41161-109">The **Get-AzureRmLocationBasedServicesAccount** cmdlet gets a provisioned Location Based Services account, either by resource group and name, or by resource id.</span></span>

<span data-ttu-id="41161-110">Darüber hinaus kann Sie eine Liste aller Konten in der ResourceGroup oder alle standortbasierten Dienstkonten für das aktuelle Abonnement zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="41161-110">Additionally, it can return a list of all accounts in the ResourceGroup, or all Location Based Services accounts for the current subscription.</span></span>

## <span data-ttu-id="41161-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="41161-111">EXAMPLES</span></span>

### <span data-ttu-id="41161-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="41161-112">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="41161-113">Ruft das Konto mit dem Namen MyAccount in der Ressourcengruppe myresourcegroup ab, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="41161-113">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="41161-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="41161-114">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="41161-115">Ruft alle standortbasierten Dienstkonten in der Ressourcengruppe myresourcegroup ab.</span><span class="sxs-lookup"><span data-stu-id="41161-115">Gets all Location Based Services accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="41161-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="41161-116">Example 3</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="41161-117">Ruft alle standortbasierten Dienstkonten im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="41161-117">Gets all Location Based Services accounts in the current subscription.</span></span>

### <span data-ttu-id="41161-118">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="41161-118">Example 4</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="41161-119">Ruft das von der Ressourcen-ID angegebene standortbasierte Dienstkonto ab.</span><span class="sxs-lookup"><span data-stu-id="41161-119">Gets the Location Based Services account specified by the Resource Id.</span></span>

## <span data-ttu-id="41161-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="41161-120">PARAMETERS</span></span>

### <span data-ttu-id="41161-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41161-121">-DefaultProfile</span></span>
<span data-ttu-id="41161-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="41161-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41161-123">-Name</span><span class="sxs-lookup"><span data-stu-id="41161-123">-Name</span></span>
<span data-ttu-id="41161-124">Name des standortbasierten Services-Kontos</span><span class="sxs-lookup"><span data-stu-id="41161-124">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41161-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41161-125">-ResourceGroupName</span></span>
<span data-ttu-id="41161-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="41161-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41161-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="41161-127">-ResourceId</span></span>
<span data-ttu-id="41161-128">Location based Services-Konto-Resourcen-Nr.</span><span class="sxs-lookup"><span data-stu-id="41161-128">Location Based Services Account ResourceId.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41161-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41161-129">CommonParameters</span></span>
<span data-ttu-id="41161-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41161-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41161-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41161-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41161-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="41161-132">INPUTS</span></span>

### <span data-ttu-id="41161-133">System. String</span><span class="sxs-lookup"><span data-stu-id="41161-133">System.String</span></span>

## <span data-ttu-id="41161-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="41161-134">OUTPUTS</span></span>

### <span data-ttu-id="41161-135">Microsoft. Azure. Commands. LocationBasedServices. Models. PSLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="41161-135">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>
<span data-ttu-id="41161-136">Dieses Cmdlet gibt ein **PSLocationBasedServicesAccount** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="41161-136">This cmdlet returns a **PSLocationBasedServicesAccount** object.</span></span>
<span data-ttu-id="41161-137">Sie können dieses Objekt ändern und dann Änderungen mithilfe von " **Satz-AzureRmLocationBasedServices** " anwenden.</span><span class="sxs-lookup"><span data-stu-id="41161-137">You can modify this object, and then apply changes by using **Set-AzureRmLocationBasedServices**.</span></span>

## <span data-ttu-id="41161-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="41161-138">NOTES</span></span>

## <span data-ttu-id="41161-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="41161-139">RELATED LINKS</span></span>
