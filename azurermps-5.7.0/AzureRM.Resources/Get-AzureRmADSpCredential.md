---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADSpCredential.md
ms.openlocfilehash: 8c03dd19fd2995347a3b4ae52de04fdcb3f02c30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663050"
---
# <span data-ttu-id="63097-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="63097-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="63097-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="63097-102">SYNOPSIS</span></span>
<span data-ttu-id="63097-103">Ruft eine Liste mit Anmeldeinformationen ab, die einem Dienstprinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="63097-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63097-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="63097-104">SYNTAX</span></span>

### <span data-ttu-id="63097-105">ObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="63097-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63097-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="63097-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63097-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63097-107">DESCRIPTION</span></span>
<span data-ttu-id="63097-108">Mithilfe des Get-AzureRmADSpCredential-Cmdlets können Sie eine Liste mit Anmeldeinformationen abrufen, die einem Dienstprinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="63097-108">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="63097-109">Dieser Befehl ruft alle Anmelde Informationseigenschaften (aber nicht den Anmelde Informationswert) ab, die dem Dienstprinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="63097-109">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="63097-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63097-110">EXAMPLES</span></span>

### <span data-ttu-id="63097-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="63097-111">Example 1</span></span>
```
PS E:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="63097-112">Gibt eine Liste der Anmeldeinformationen zurück, die dem Dienstprinzipal mit SPN ' ' zugeordnet sind http://test12345 .</span><span class="sxs-lookup"><span data-stu-id="63097-112">Returns a list of credentials associated with the service principal having SPN 'http://test12345'.</span></span>

## <span data-ttu-id="63097-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="63097-113">PARAMETERS</span></span>

### <span data-ttu-id="63097-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63097-114">-DefaultProfile</span></span>
<span data-ttu-id="63097-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="63097-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63097-116">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="63097-116">-ObjectId</span></span>
<span data-ttu-id="63097-117">Die Objekt-ID des Dienst Prinzipals, von dem die Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="63097-117">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63097-118">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="63097-118">-ServicePrincipalName</span></span>
<span data-ttu-id="63097-119">Der Name (SPN) des Dienst Prinzipals, aus dem Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="63097-119">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63097-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63097-120">CommonParameters</span></span>
<span data-ttu-id="63097-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63097-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63097-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63097-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63097-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="63097-123">INPUTS</span></span>

### <span data-ttu-id="63097-124">Keine</span><span class="sxs-lookup"><span data-stu-id="63097-124">None</span></span>
<span data-ttu-id="63097-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="63097-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="63097-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="63097-126">OUTPUTS</span></span>

### <span data-ttu-id="63097-127">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="63097-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="63097-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="63097-128">NOTES</span></span>

## <span data-ttu-id="63097-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="63097-129">RELATED LINKS</span></span>

[<span data-ttu-id="63097-130">Neu – AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="63097-130">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="63097-131">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="63097-131">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="63097-132">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="63097-132">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

