---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: ba169c54d2b4664473a0013be52e2d078827dcb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495729"
---
# <span data-ttu-id="80b7f-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="80b7f-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="80b7f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="80b7f-103">Ruft eine Liste der Anmeldeinformationen ab, die einer Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="80b7f-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80b7f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80b7f-104">SYNTAX</span></span>

### <span data-ttu-id="80b7f-105">ApplicationObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="80b7f-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80b7f-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80b7f-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="80b7f-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="80b7f-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="80b7f-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80b7f-108">ApplicationObjectParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80b7f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80b7f-109">DESCRIPTION</span></span>
<span data-ttu-id="80b7f-110">Das Get-AzureRmADAppCredential-Cmdlet kann verwendet werden, um eine Liste der Anmeldeinformationen abzurufen, die einer Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="80b7f-110">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="80b7f-111">Dieser Befehl ruft alle Anmelde Informationseigenschaften (aber nicht den Wert der Anmeldeinformationen) ab, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="80b7f-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="80b7f-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80b7f-112">EXAMPLES</span></span>

### <span data-ttu-id="80b7f-113">Beispiel 1: Abrufen von Anwendungs Anmeldeinformationen nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="80b7f-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="80b7f-114">Gibt eine Liste der Anmeldeinformationen zurück, die der Anwendung zugeordnet sind, die die Objekt-ID "1f99cf81-0146-4f4e-BEAE-2007d0668476" hat.</span><span class="sxs-lookup"><span data-stu-id="80b7f-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="80b7f-115">Beispiel 2 – Abrufen von Anwendungs Anmeldeinformationen durch Piping</span><span class="sxs-lookup"><span data-stu-id="80b7f-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzureRmADAppCredential
```

<span data-ttu-id="80b7f-116">Ruft die Anwendung mit der Objekt-ID "1f99cf81-0146-4f4e-BEAE-2007d0668476" ab und leitet Sie an das Get-AzureRmADAppCredential-Cmdlet weiter, um alle Anmeldeinformationen für diese Anwendung aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="80b7f-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzureRmADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="80b7f-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="80b7f-117">PARAMETERS</span></span>

### <span data-ttu-id="80b7f-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="80b7f-118">-ApplicationId</span></span>
<span data-ttu-id="80b7f-119">Die ID der Anwendung, aus der Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="80b7f-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="80b7f-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="80b7f-120">-ApplicationObject</span></span>
<span data-ttu-id="80b7f-121">Das Application-Objekt, aus dem Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="80b7f-121">The application object to retrieve credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80b7f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80b7f-122">-DefaultProfile</span></span>
<span data-ttu-id="80b7f-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="80b7f-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80b7f-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="80b7f-124">-DisplayName</span></span>
<span data-ttu-id="80b7f-125">Der Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="80b7f-125">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80b7f-126">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="80b7f-126">-ObjectId</span></span>
<span data-ttu-id="80b7f-127">Die Objekt-ID der Anwendung, aus der Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="80b7f-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="80b7f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b7f-128">CommonParameters</span></span>
<span data-ttu-id="80b7f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80b7f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b7f-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80b7f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b7f-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80b7f-131">INPUTS</span></span>

### <span data-ttu-id="80b7f-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="80b7f-132">System.Guid</span></span>

### <span data-ttu-id="80b7f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="80b7f-133">System.String</span></span>

### <span data-ttu-id="80b7f-134">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="80b7f-134">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="80b7f-135">Parameter: applicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="80b7f-135">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="80b7f-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80b7f-136">OUTPUTS</span></span>

### <span data-ttu-id="80b7f-137">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="80b7f-137">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="80b7f-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="80b7f-138">NOTES</span></span>

## <span data-ttu-id="80b7f-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80b7f-139">RELATED LINKS</span></span>

[<span data-ttu-id="80b7f-140">Neu – AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="80b7f-140">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="80b7f-141">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="80b7f-141">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="80b7f-142">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="80b7f-142">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

