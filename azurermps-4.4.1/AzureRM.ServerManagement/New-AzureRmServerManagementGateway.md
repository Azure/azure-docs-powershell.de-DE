---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: 9cb98b9671f43ddd7acbcc84e8473a12da00f405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496873"
---
# <span data-ttu-id="88138-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="88138-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="88138-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="88138-102">SYNOPSIS</span></span>
<span data-ttu-id="88138-103">Erstellt ein Server Verwaltungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="88138-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88138-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="88138-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88138-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88138-105">DESCRIPTION</span></span>
<span data-ttu-id="88138-106">Das Cmdlet **New-AzureRmServerManagementGateway** erstellt ein Azure Server-Verwaltungs Gateway.</span><span class="sxs-lookup"><span data-stu-id="88138-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="88138-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88138-107">EXAMPLES</span></span>

## <span data-ttu-id="88138-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="88138-108">PARAMETERS</span></span>

### <span data-ttu-id="88138-109">-AutoUpgrade</span><span class="sxs-lookup"><span data-stu-id="88138-109">-AutoUpgrade</span></span>
<span data-ttu-id="88138-110">Gibt an, dass das Gateway automatisch ein Upgrade durchführt, wenn eine neue Version freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="88138-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

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

### <span data-ttu-id="88138-111">-Gatewayname</span><span class="sxs-lookup"><span data-stu-id="88138-111">-GatewayName</span></span>
<span data-ttu-id="88138-112">Gibt den Namen des Gateways an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="88138-112">Specifies the name of the gateway that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88138-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="88138-113">-Location</span></span>
<span data-ttu-id="88138-114">Gibt den Speicherort an, an dem das Gateway erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="88138-114">Specifies the location in which to create the gateway.</span></span>

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

### <span data-ttu-id="88138-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88138-115">-ResourceGroupName</span></span>
<span data-ttu-id="88138-116">Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet das Gateway erstellt.</span><span class="sxs-lookup"><span data-stu-id="88138-116">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

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

### <span data-ttu-id="88138-117">-Tags</span><span class="sxs-lookup"><span data-stu-id="88138-117">-Tags</span></span>
<span data-ttu-id="88138-118">Gibt Tags als Schlüssel-Wert-Paare an.</span><span class="sxs-lookup"><span data-stu-id="88138-118">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="88138-119">Sie können mithilfe von Tags ein Gateway aus anderen Azure-Ressourcen identifizieren.</span><span class="sxs-lookup"><span data-stu-id="88138-119">You can use tags to identify a Gateway from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88138-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88138-120">-DefaultProfile</span></span>
<span data-ttu-id="88138-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="88138-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88138-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88138-122">CommonParameters</span></span>
<span data-ttu-id="88138-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88138-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88138-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88138-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88138-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="88138-125">INPUTS</span></span>

## <span data-ttu-id="88138-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="88138-126">OUTPUTS</span></span>

### <span data-ttu-id="88138-127">Microsoft. Azure. Commands. Servermanagement. Model. Gateway</span><span class="sxs-lookup"><span data-stu-id="88138-127">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="88138-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="88138-128">NOTES</span></span>

## <span data-ttu-id="88138-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="88138-129">RELATED LINKS</span></span>

[<span data-ttu-id="88138-130">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="88138-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="88138-131">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="88138-131">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


