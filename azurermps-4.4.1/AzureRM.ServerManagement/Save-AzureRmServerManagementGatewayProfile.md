---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: ECF85C07-2C9E-487D-A2ED-77875C380244
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: af7184b3e43d2016ff4acc9e7634f831945a8fdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501610"
---
# <span data-ttu-id="7490f-101">Save-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="7490f-101">Save-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="7490f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7490f-102">SYNOPSIS</span></span>
<span data-ttu-id="7490f-103">Lädt das Profil für ein Server Verwaltungs Gateway herunter und speichert es in einer lokalen Datei.</span><span class="sxs-lookup"><span data-stu-id="7490f-103">Downloads the profile for a Server Management gateway and saves it to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7490f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7490f-104">SYNTAX</span></span>

### <span data-ttu-id="7490f-105">ByName</span><span class="sxs-lookup"><span data-stu-id="7490f-105">ByName</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-ResourceGroupName] <String>
 [-GatewayName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7490f-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="7490f-106">ByObject</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-Gateway] <Gateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7490f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7490f-107">DESCRIPTION</span></span>
<span data-ttu-id="7490f-108">Das Cmdlet **Save-AzureRmServerManagementGatewayProfile** downloadet das Profil für ein Azure Server-Verwaltungs Gateway und speichert es in einer lokalen Datei.</span><span class="sxs-lookup"><span data-stu-id="7490f-108">The **Save-AzureRmServerManagementGatewayProfile** cmdlet downloads the profile for an Azure Server Management gateway and stores it to a local file.</span></span>

## <span data-ttu-id="7490f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7490f-109">EXAMPLES</span></span>

## <span data-ttu-id="7490f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7490f-110">PARAMETERS</span></span>

### <span data-ttu-id="7490f-111">-Gateway</span><span class="sxs-lookup"><span data-stu-id="7490f-111">-Gateway</span></span>
<span data-ttu-id="7490f-112">Gibt das Gateway an, für das dieses Cmdlet das Profil erhält.</span><span class="sxs-lookup"><span data-stu-id="7490f-112">Specifies the gateway that this cmdlet gets the profile for.</span></span>

<span data-ttu-id="7490f-113">Kann verwendet werden, anstatt ResourceGroupName und Gatewayname anzugeben</span><span class="sxs-lookup"><span data-stu-id="7490f-113">May be used instead of specifying ResourceGroupName and GatewayName</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7490f-114">-Gatewayname</span><span class="sxs-lookup"><span data-stu-id="7490f-114">-GatewayName</span></span>
<span data-ttu-id="7490f-115">Gibt den Namen des Gateways an, für das dieses Cmdlet das Profil erhält.</span><span class="sxs-lookup"><span data-stu-id="7490f-115">Specifies the name of the gateway that this cmdlet gets the profile for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7490f-116">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="7490f-116">-OutputFile</span></span>
<span data-ttu-id="7490f-117">Gibt die lokale Datei an, in der die Profildaten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7490f-117">Specifies the local file in which to save the profile data.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7490f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7490f-118">-ResourceGroupName</span></span>
<span data-ttu-id="7490f-119">Gibt den Namen der Ressourcengruppe an, zu der das Gateway gehört.</span><span class="sxs-lookup"><span data-stu-id="7490f-119">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7490f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7490f-120">-DefaultProfile</span></span>
<span data-ttu-id="7490f-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7490f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7490f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7490f-122">CommonParameters</span></span>
<span data-ttu-id="7490f-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7490f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7490f-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7490f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7490f-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7490f-125">INPUTS</span></span>

### <span data-ttu-id="7490f-126">Gateway</span><span class="sxs-lookup"><span data-stu-id="7490f-126">Gateway</span></span>
<span data-ttu-id="7490f-127">Der Parameter "Gateway" akzeptiert den Wert vom Typ "Gateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7490f-127">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="7490f-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7490f-128">OUTPUTS</span></span>

### <span data-ttu-id="7490f-129">System. IO. FileInfo</span><span class="sxs-lookup"><span data-stu-id="7490f-129">System.IO.FileInfo</span></span>

## <span data-ttu-id="7490f-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="7490f-130">NOTES</span></span>

## <span data-ttu-id="7490f-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7490f-131">RELATED LINKS</span></span>

[<span data-ttu-id="7490f-132">Installieren-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="7490f-132">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="7490f-133">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="7490f-133">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)


