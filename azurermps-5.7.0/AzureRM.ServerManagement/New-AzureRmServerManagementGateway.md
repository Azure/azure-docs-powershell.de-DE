---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: f73d53fc3031fc72be950547e5b9c2b93a9a0079
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662564"
---
# <span data-ttu-id="21b13-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="21b13-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="21b13-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21b13-102">SYNOPSIS</span></span>
<span data-ttu-id="21b13-103">Erstellt ein Server Verwaltungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="21b13-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21b13-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21b13-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21b13-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21b13-105">DESCRIPTION</span></span>
<span data-ttu-id="21b13-106">Das Cmdlet **New-AzureRmServerManagementGateway** erstellt ein Azure Server-Verwaltungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="21b13-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="21b13-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21b13-107">EXAMPLES</span></span>

## <span data-ttu-id="21b13-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="21b13-108">PARAMETERS</span></span>

### <span data-ttu-id="21b13-109">-AutoUpgrade</span><span class="sxs-lookup"><span data-stu-id="21b13-109">-AutoUpgrade</span></span>
<span data-ttu-id="21b13-110">Gibt an, dass das Gateway automatisch ein Upgrade durchführt, wenn eine neue Version freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="21b13-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

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

### <span data-ttu-id="21b13-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21b13-111">-DefaultProfile</span></span>
<span data-ttu-id="21b13-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="21b13-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21b13-113">-Gatewayname</span><span class="sxs-lookup"><span data-stu-id="21b13-113">-GatewayName</span></span>
<span data-ttu-id="21b13-114">Gibt den Namen des Gateways an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="21b13-114">Specifies the name of the gateway that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21b13-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="21b13-115">-Location</span></span>
<span data-ttu-id="21b13-116">Gibt den Speicherort an, an dem das Gateway erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="21b13-116">Specifies the location in which to create the gateway.</span></span>

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

### <span data-ttu-id="21b13-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21b13-117">-ResourceGroupName</span></span>
<span data-ttu-id="21b13-118">Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet das Gateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="21b13-118">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

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

### <span data-ttu-id="21b13-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="21b13-119">-Tag</span></span>
<span data-ttu-id="21b13-120">Schlüssel-Wert-Paare, die dem Gateway zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="21b13-120">Key/value pairs associated with the gateway.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21b13-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21b13-121">CommonParameters</span></span>
<span data-ttu-id="21b13-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21b13-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21b13-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21b13-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21b13-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21b13-124">INPUTS</span></span>

### <span data-ttu-id="21b13-125">Keine</span><span class="sxs-lookup"><span data-stu-id="21b13-125">None</span></span>
<span data-ttu-id="21b13-126">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="21b13-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="21b13-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21b13-127">OUTPUTS</span></span>

### <span data-ttu-id="21b13-128">Microsoft. Azure. Commands. Servermanagement. Model. Gateway</span><span class="sxs-lookup"><span data-stu-id="21b13-128">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="21b13-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="21b13-129">NOTES</span></span>

## <span data-ttu-id="21b13-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21b13-130">RELATED LINKS</span></span>

[<span data-ttu-id="21b13-131">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="21b13-131">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="21b13-132">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="21b13-132">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


