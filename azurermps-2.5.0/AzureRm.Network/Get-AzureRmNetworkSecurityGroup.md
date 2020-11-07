---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: e0a9bd49ca49ae4df1ae83d9c93a191f406c442a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848164"
---
# <span data-ttu-id="83baf-101">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="83baf-101">Get-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="83baf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83baf-102">SYNOPSIS</span></span>
<span data-ttu-id="83baf-103">Ruft eine Netzwerksicherheitsgruppe ab.</span><span class="sxs-lookup"><span data-stu-id="83baf-103">Gets a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83baf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83baf-104">SYNTAX</span></span>

### <span data-ttu-id="83baf-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="83baf-105">NoExpand</span></span>
```
Get-AzureRmNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83baf-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="83baf-106">Expand</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83baf-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83baf-107">DESCRIPTION</span></span>
<span data-ttu-id="83baf-108">Das Cmdlet " **Get-AzureRmNetworkSecurityGroup** " Ruft eine Azure Network Security-Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="83baf-108">The **Get-AzureRmNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="83baf-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83baf-109">EXAMPLES</span></span>

### <span data-ttu-id="83baf-110">1: Abrufen einer vorhandenen Netzwerksicherheitsgruppe</span><span class="sxs-lookup"><span data-stu-id="83baf-110">1: Retrieve an existing network security group</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName "rg1"
```

<span data-ttu-id="83baf-111">Dieser Befehl gibt den Inhalt der Azure Network Security-Gruppe "nsg1" in der Ressourcengruppe "RG1" zurück.</span><span class="sxs-lookup"><span data-stu-id="83baf-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="83baf-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="83baf-112">PARAMETERS</span></span>

### <span data-ttu-id="83baf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83baf-113">-DefaultProfile</span></span>
<span data-ttu-id="83baf-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="83baf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83baf-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="83baf-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83baf-116">-Name</span><span class="sxs-lookup"><span data-stu-id="83baf-116">-Name</span></span>
<span data-ttu-id="83baf-117">Gibt den Namen der Netzwerksicherheitsgruppe an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="83baf-117">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83baf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83baf-118">-ResourceGroupName</span></span>
<span data-ttu-id="83baf-119">Gibt den Namen der Ressourcengruppe an, zu der die Netzwerksicherheitsgruppe gehört.</span><span class="sxs-lookup"><span data-stu-id="83baf-119">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83baf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83baf-120">CommonParameters</span></span>
<span data-ttu-id="83baf-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83baf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83baf-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83baf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83baf-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83baf-123">INPUTS</span></span>

## <span data-ttu-id="83baf-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83baf-124">OUTPUTS</span></span>

### <span data-ttu-id="83baf-125">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="83baf-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="83baf-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="83baf-126">NOTES</span></span>

## <span data-ttu-id="83baf-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83baf-127">RELATED LINKS</span></span>

[<span data-ttu-id="83baf-128">Neu – AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="83baf-128">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="83baf-129">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="83baf-129">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="83baf-130">Satz-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="83baf-130">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


