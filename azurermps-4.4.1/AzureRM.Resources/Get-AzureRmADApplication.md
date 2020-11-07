---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: c5276ddbcd10870355f8530c2f04f81122dda382
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662901"
---
# <span data-ttu-id="64845-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="64845-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="64845-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64845-102">SYNOPSIS</span></span>
<span data-ttu-id="64845-103">Listet vorhandene Azure Active Directory-Anwendungen auf.</span><span class="sxs-lookup"><span data-stu-id="64845-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64845-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="64845-104">SYNTAX</span></span>

### <span data-ttu-id="64845-105">EmptyParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="64845-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64845-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="64845-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64845-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="64845-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64845-108">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="64845-108">ApplicationDisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64845-109">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="64845-109">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64845-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64845-110">DESCRIPTION</span></span>
<span data-ttu-id="64845-111">Listet vorhandene Azure Active Directory-Anwendungen auf.</span><span class="sxs-lookup"><span data-stu-id="64845-111">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="64845-112">Die Anwendungssuche kann über ObjectID, ApplicationId, IdentifierUri oder DisplayName erfolgen.</span><span class="sxs-lookup"><span data-stu-id="64845-112">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="64845-113">Wenn kein Parameter angegeben wird, werden alle Anwendungen unter dem Mandanten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="64845-113">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="64845-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64845-114">EXAMPLES</span></span>

### <span data-ttu-id="64845-115">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="64845-115">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADApplication
```

<span data-ttu-id="64845-116">Listet alle Anwendungen unter einem Mandanten auf.</span><span class="sxs-lookup"><span data-stu-id="64845-116">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="64845-117">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="64845-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="64845-118">Ruft die Anwendung mit dem Bezeichner-URI als " http://mySecretApp1 " ab.</span><span class="sxs-lookup"><span data-stu-id="64845-118">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

## <span data-ttu-id="64845-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="64845-119">PARAMETERS</span></span>

### <span data-ttu-id="64845-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="64845-120">-ApplicationId</span></span>
<span data-ttu-id="64845-121">Die Anwendungs-ID der Anwendung, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="64845-121">The application id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64845-122">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="64845-122">-DisplayNameStartWith</span></span>
<span data-ttu-id="64845-123">Ruft alle Anwendungen ab, beginnend mit dem Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="64845-123">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64845-124">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="64845-124">-IdentifierUri</span></span>
<span data-ttu-id="64845-125">Eindeutiger Bezeichner-URI der Anwendung, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="64845-125">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64845-126">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="64845-126">-ObjectId</span></span>
<span data-ttu-id="64845-127">Die Objekt-ID der abzurufenden Anwendung.</span><span class="sxs-lookup"><span data-stu-id="64845-127">The object id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64845-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64845-128">-DefaultProfile</span></span>
<span data-ttu-id="64845-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="64845-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64845-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64845-130">CommonParameters</span></span>
<span data-ttu-id="64845-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64845-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64845-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64845-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64845-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64845-133">INPUTS</span></span>

## <span data-ttu-id="64845-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64845-134">OUTPUTS</span></span>

### <span data-ttu-id="64845-135">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication]</span><span class="sxs-lookup"><span data-stu-id="64845-135">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication]</span></span>

## <span data-ttu-id="64845-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="64845-136">NOTES</span></span>

## <span data-ttu-id="64845-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64845-137">RELATED LINKS</span></span>

[<span data-ttu-id="64845-138">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="64845-138">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="64845-139">Neu – AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="64845-139">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="64845-140">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="64845-140">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="64845-141">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="64845-141">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="64845-142">Satz-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="64845-142">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="64845-143">Neu – AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="64845-143">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

