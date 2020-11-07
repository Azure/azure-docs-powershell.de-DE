---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 772f0a3bb1198bf5c8d00ad8c0dd708c37c92366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662678"
---
# <span data-ttu-id="67de9-101">Get-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="67de9-101">Get-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="67de9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67de9-102">SYNOPSIS</span></span>
<span data-ttu-id="67de9-103">Ruft ein öffentliches IP-Präfix ab</span><span class="sxs-lookup"><span data-stu-id="67de9-103">Gets a public IP prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67de9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67de9-104">SYNTAX</span></span>

### <span data-ttu-id="67de9-105">Standard</span><span class="sxs-lookup"><span data-stu-id="67de9-105">(Default)</span></span>
```
Get-AzureRmPublicIpPrefix [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67de9-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="67de9-106">GetByNameParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67de9-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67de9-107">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67de9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67de9-108">DESCRIPTION</span></span>
<span data-ttu-id="67de9-109">Das Cmdlet " **Get-AzureRmPublicIpPrefix** " ruft mindestens ein öffentliches IP-Präfix in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="67de9-109">The **Get-AzureRmPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="67de9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67de9-110">EXAMPLES</span></span>

### <span data-ttu-id="67de9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="67de9-111">Example 1</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -ResourceGroupName $rgname -Name $prefixName
```

<span data-ttu-id="67de9-112">Mit diesem Befehl wird eine öffentliche IP-Präfix Ressource mit $prefixName in der Ressourcengruppe abgerufen $rgName</span><span class="sxs-lookup"><span data-stu-id="67de9-112">This command gets a public IP prefix resource with $prefixName in resource group $rgName</span></span>

## <span data-ttu-id="67de9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="67de9-113">PARAMETERS</span></span>

### <span data-ttu-id="67de9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67de9-114">-DefaultProfile</span></span>
<span data-ttu-id="67de9-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="67de9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67de9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="67de9-116">-Name</span></span>
<span data-ttu-id="67de9-117">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="67de9-117">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67de9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67de9-118">-ResourceGroupName</span></span>
<span data-ttu-id="67de9-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="67de9-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67de9-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="67de9-120">-ResourceId</span></span>
<span data-ttu-id="67de9-121">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="67de9-121">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67de9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67de9-122">CommonParameters</span></span>
<span data-ttu-id="67de9-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67de9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="67de9-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67de9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67de9-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67de9-125">INPUTS</span></span>

### <span data-ttu-id="67de9-126">System. String</span><span class="sxs-lookup"><span data-stu-id="67de9-126">System.String</span></span>


## <span data-ttu-id="67de9-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67de9-127">OUTPUTS</span></span>

### <span data-ttu-id="67de9-128">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="67de9-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="67de9-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="67de9-129">NOTES</span></span>

## <span data-ttu-id="67de9-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67de9-130">RELATED LINKS</span></span>
