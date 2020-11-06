---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkProfile.md
ms.openlocfilehash: 5bdd5e5d5212564afb1f9b06f220e8c452bcbbaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505757"
---
# <span data-ttu-id="f9cec-101">Get-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f9cec-101">Get-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="f9cec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9cec-102">SYNOPSIS</span></span>
<span data-ttu-id="f9cec-103">Ruft eine vorhandene Netzwerkprofil-Ressource auf oberster Ebene ab</span><span class="sxs-lookup"><span data-stu-id="f9cec-103">Gets an existing network profile top level resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9cec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9cec-104">SYNTAX</span></span>

### <span data-ttu-id="f9cec-105">NOEXPAND (Standard)</span><span class="sxs-lookup"><span data-stu-id="f9cec-105">NoExpand (Default)</span></span>
```
Get-AzureRmNetworkProfile [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9cec-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9cec-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9cec-107">GetByResourceNameNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9cec-107">GetByResourceNameNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile [-ResourceGroupName <String>] [-Name <String>] -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9cec-108">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9cec-108">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9cec-109">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9cec-109">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzureRmNetworkProfile -ResourceId <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9cec-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9cec-110">DESCRIPTION</span></span>
<span data-ttu-id="f9cec-111">Das Cmdlet " **Get-AzureRmNetworkProfile** " Ruft eine vorhandene Netzwerkprofil Ressource auf oberster Ebene ab</span><span class="sxs-lookup"><span data-stu-id="f9cec-111">The **Get-AzureRmNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="f9cec-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9cec-112">EXAMPLES</span></span>

### <span data-ttu-id="f9cec-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f9cec-113">Example 1</span></span>
```powershell
$networkProfile = Get-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="f9cec-114">Dadurch wird das Netzwerkprofil-Np1 in der Ressourcengruppe abgerufen RG1</span><span class="sxs-lookup"><span data-stu-id="f9cec-114">This retrieves the network profile np1 in resource group rg1</span></span>

## <span data-ttu-id="f9cec-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9cec-115">PARAMETERS</span></span>

### <span data-ttu-id="f9cec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9cec-116">-DefaultProfile</span></span>
<span data-ttu-id="f9cec-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f9cec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9cec-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f9cec-118">-ExpandResource</span></span>
<span data-ttu-id="f9cec-119">Der Ressourcenverweis, der erweitert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9cec-119">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceNameNoExpandParameterSet, GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9cec-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f9cec-120">-Name</span></span>
<span data-ttu-id="f9cec-121">Der Name des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="f9cec-121">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9cec-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9cec-122">-ResourceGroupName</span></span>
<span data-ttu-id="f9cec-123">Der Ressourcengruppenname des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="f9cec-123">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9cec-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f9cec-124">-ResourceId</span></span>
<span data-ttu-id="f9cec-125">Die Azure Resource Manager-ID des Netzwerkprofils.</span><span class="sxs-lookup"><span data-stu-id="f9cec-125">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9cec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9cec-126">CommonParameters</span></span>
<span data-ttu-id="f9cec-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9cec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9cec-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9cec-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9cec-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9cec-129">INPUTS</span></span>

### <span data-ttu-id="f9cec-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f9cec-130">System.String</span></span>

## <span data-ttu-id="f9cec-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9cec-131">OUTPUTS</span></span>

### <span data-ttu-id="f9cec-132">Microsoft. Azure. Commands. Network. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f9cec-132">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="f9cec-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9cec-133">NOTES</span></span>

## <span data-ttu-id="f9cec-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9cec-134">RELATED LINKS</span></span>
