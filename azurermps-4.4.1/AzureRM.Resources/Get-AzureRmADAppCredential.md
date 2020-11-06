---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: e270a59e3799302eed49a0fd60180bb8d4589d92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504769"
---
# <span data-ttu-id="9331c-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9331c-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="9331c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9331c-102">SYNOPSIS</span></span>
<span data-ttu-id="9331c-103">Ruft eine Liste der Anmeldeinformationen ab, die einer Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9331c-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9331c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9331c-104">SYNTAX</span></span>

### <span data-ttu-id="9331c-105">ApplicationObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="9331c-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9331c-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9331c-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9331c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9331c-107">DESCRIPTION</span></span>
<span data-ttu-id="9331c-108">Das Get-AzureRmADAppCredential-Cmdlet kann verwendet werden, um eine Liste der Anmeldeinformationen abzurufen, die einer Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9331c-108">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>

<span data-ttu-id="9331c-109">Dieser Befehl ruft alle Anmelde Informationseigenschaften (aber nicht den Wert der Anmeldeinformationen) ab, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9331c-109">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="9331c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9331c-110">EXAMPLES</span></span>

### <span data-ttu-id="9331c-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9331c-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="9331c-112">Gibt eine Liste der Anmeldeinformationen zurück, die der Anwendung zugeordnet sind, die die Objekt-ID "1f99cf81-0146-4f4e-BEAE-2007d0668476" hat.</span><span class="sxs-lookup"><span data-stu-id="9331c-112">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

## <span data-ttu-id="9331c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9331c-113">PARAMETERS</span></span>

### <span data-ttu-id="9331c-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9331c-114">-ApplicationId</span></span>
<span data-ttu-id="9331c-115">Die ID der Anwendung, aus der Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9331c-115">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9331c-116">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="9331c-116">-ObjectId</span></span>
<span data-ttu-id="9331c-117">Die Objekt-ID der Anwendung, aus der Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9331c-117">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9331c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9331c-118">-DefaultProfile</span></span>
<span data-ttu-id="9331c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9331c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9331c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9331c-120">CommonParameters</span></span>
<span data-ttu-id="9331c-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9331c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9331c-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9331c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9331c-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9331c-123">INPUTS</span></span>

## <span data-ttu-id="9331c-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9331c-124">OUTPUTS</span></span>

### <span data-ttu-id="9331c-125">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="9331c-125">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="9331c-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="9331c-126">NOTES</span></span>

## <span data-ttu-id="9331c-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9331c-127">RELATED LINKS</span></span>

[<span data-ttu-id="9331c-128">Neu – AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9331c-128">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="9331c-129">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9331c-129">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="9331c-130">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="9331c-130">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

