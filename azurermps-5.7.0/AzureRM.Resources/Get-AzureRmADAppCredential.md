---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: fa2368e1982e66d8edecc465d1f6ded3a3d75205
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482753"
---
# <span data-ttu-id="7e85f-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7e85f-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="7e85f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e85f-102">SYNOPSIS</span></span>
<span data-ttu-id="7e85f-103">Ruft eine Liste der Anmeldeinformationen ab, die einer Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7e85f-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e85f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e85f-104">SYNTAX</span></span>

### <span data-ttu-id="7e85f-105">ApplicationObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7e85f-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e85f-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e85f-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e85f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e85f-107">DESCRIPTION</span></span>
<span data-ttu-id="7e85f-108">Das Get-AzureRmADAppCredential-Cmdlet kann verwendet werden, um eine Liste der Anmeldeinformationen abzurufen, die einer Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7e85f-108">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>

<span data-ttu-id="7e85f-109">Dieser Befehl ruft alle Anmelde Informationseigenschaften (aber nicht den Wert der Anmeldeinformationen) ab, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7e85f-109">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="7e85f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e85f-110">EXAMPLES</span></span>

### <span data-ttu-id="7e85f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7e85f-111">Example 1</span></span>
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="7e85f-112">Gibt eine Liste der Anmeldeinformationen zurück, die der Anwendung zugeordnet sind, die die Objekt-ID "1f99cf81-0146-4f4e-BEAE-2007d0668476" hat.</span><span class="sxs-lookup"><span data-stu-id="7e85f-112">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

## <span data-ttu-id="7e85f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e85f-113">PARAMETERS</span></span>

### <span data-ttu-id="7e85f-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7e85f-114">-ApplicationId</span></span>
<span data-ttu-id="7e85f-115">Die ID der Anwendung, aus der Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7e85f-115">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e85f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e85f-116">-DefaultProfile</span></span>
<span data-ttu-id="7e85f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7e85f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e85f-118">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="7e85f-118">-ObjectId</span></span>
<span data-ttu-id="7e85f-119">Die Objekt-ID der Anwendung, aus der Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7e85f-119">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e85f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e85f-120">CommonParameters</span></span>
<span data-ttu-id="7e85f-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e85f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e85f-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e85f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e85f-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e85f-123">INPUTS</span></span>

### <span data-ttu-id="7e85f-124">Keine</span><span class="sxs-lookup"><span data-stu-id="7e85f-124">None</span></span>
<span data-ttu-id="7e85f-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7e85f-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7e85f-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e85f-126">OUTPUTS</span></span>

### <span data-ttu-id="7e85f-127">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="7e85f-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="7e85f-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e85f-128">NOTES</span></span>

## <span data-ttu-id="7e85f-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e85f-129">RELATED LINKS</span></span>

[<span data-ttu-id="7e85f-130">Neu – AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7e85f-130">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="7e85f-131">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7e85f-131">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="7e85f-132">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="7e85f-132">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

