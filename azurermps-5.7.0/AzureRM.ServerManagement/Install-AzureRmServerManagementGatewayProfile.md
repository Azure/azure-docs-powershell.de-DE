---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 06081209-BBE5-4F76-86F8-9CF6197938F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/install-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: b9563e9b8b7afb7b980f0b3cd307c76fb9c6e8be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480929"
---
# <span data-ttu-id="f46a8-101">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="f46a8-101">Install-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="f46a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f46a8-102">SYNOPSIS</span></span>
<span data-ttu-id="f46a8-103">Installiert ein Server-Management-Gateway-Profil.</span><span class="sxs-lookup"><span data-stu-id="f46a8-103">Installs a Server Management Gateway profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f46a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f46a8-104">SYNTAX</span></span>

```
Install-AzureRmServerManagementGatewayProfile [[-InputFile] <FileInfo>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f46a8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f46a8-105">DESCRIPTION</span></span>
<span data-ttu-id="f46a8-106">Das Cmdlet " **install-AzureRmServerManagementGatewayProfile** " installiert ein Azure Server Management Gateway-Profil am richtigen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="f46a8-106">The **Install-AzureRmServerManagementGatewayProfile** cmdlet installs an Azure Server Management Gateway profile into the correct location.</span></span>
<span data-ttu-id="f46a8-107">Die Datei, die dieses Cmdlet installiert, hat den Namen profile.json.</span><span class="sxs-lookup"><span data-stu-id="f46a8-107">The file that this cmdlet installs is named profile.json.</span></span>

## <span data-ttu-id="f46a8-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f46a8-108">EXAMPLES</span></span>

## <span data-ttu-id="f46a8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f46a8-109">PARAMETERS</span></span>

### <span data-ttu-id="f46a8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f46a8-110">-DefaultProfile</span></span>
<span data-ttu-id="f46a8-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f46a8-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f46a8-112">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="f46a8-112">-InputFile</span></span>
<span data-ttu-id="f46a8-113">Gibt den Namen der lokalen Datei an, die das zu installierende Gateway-Profil enthält.</span><span class="sxs-lookup"><span data-stu-id="f46a8-113">Specifies the name of the local file that contains the gateway profile to install.</span></span>

<span data-ttu-id="f46a8-114">Die Datei, die dieses Cmdlet installiert, sollte zuvor mit dem Save-AzureRmServerManagementGatewayProfile-Cmdlet gespeichert worden sein.</span><span class="sxs-lookup"><span data-stu-id="f46a8-114">The file that this cmdlet installs should have been previously saved with the Save-AzureRmServerManagementGatewayProfile cmdlet.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f46a8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f46a8-115">CommonParameters</span></span>
<span data-ttu-id="f46a8-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f46a8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f46a8-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f46a8-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f46a8-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f46a8-118">INPUTS</span></span>

### <span data-ttu-id="f46a8-119">FileInfo</span><span class="sxs-lookup"><span data-stu-id="f46a8-119">FileInfo</span></span>
<span data-ttu-id="f46a8-120">Der Parameter ' Inputdatei ' akzeptiert den Wert vom Typ ' FileInfo ' aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f46a8-120">Parameter 'InputFile' accepts value of type 'FileInfo' from the pipeline</span></span>

## <span data-ttu-id="f46a8-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f46a8-121">OUTPUTS</span></span>

## <span data-ttu-id="f46a8-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="f46a8-122">NOTES</span></span>

## <span data-ttu-id="f46a8-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f46a8-123">RELATED LINKS</span></span>

[<span data-ttu-id="f46a8-124">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="f46a8-124">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="f46a8-125">Save-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="f46a8-125">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


