---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: ef03850e2a8c0981ad4a1b642df51c1fec462513
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996731"
---
# <span data-ttu-id="7b93b-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7b93b-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="7b93b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b93b-102">SYNOPSIS</span></span>
<span data-ttu-id="7b93b-103">Ruft eine Liste der Anmeldeinformationen ab, die einer Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7b93b-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="7b93b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b93b-104">SYNTAX</span></span>

### <span data-ttu-id="7b93b-105">ApplicationObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7b93b-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b93b-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b93b-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b93b-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b93b-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b93b-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b93b-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b93b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b93b-109">DESCRIPTION</span></span>
<span data-ttu-id="7b93b-110">Das Get-AzADAppCredential-Cmdlet kann verwendet werden, um eine Liste der Anmeldeinformationen abzurufen, die einer Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7b93b-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="7b93b-111">Dieser Befehl ruft alle Anmelde Informationseigenschaften (aber nicht den Wert der Anmeldeinformationen) ab, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7b93b-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="7b93b-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b93b-112">EXAMPLES</span></span>

### <span data-ttu-id="7b93b-113">Beispiel 1: Abrufen von Anwendungs Anmeldeinformationen nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="7b93b-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="7b93b-114">Gibt eine Liste der Anmeldeinformationen zurück, die der Anwendung zugeordnet sind, die die Objekt-ID "1f99cf81-0146-4f4e-BEAE-2007d0668476" hat.</span><span class="sxs-lookup"><span data-stu-id="7b93b-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="7b93b-115">Beispiel 2 – Abrufen von Anwendungs Anmeldeinformationen durch Piping</span><span class="sxs-lookup"><span data-stu-id="7b93b-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="7b93b-116">Ruft die Anwendung mit der Objekt-ID "1f99cf81-0146-4f4e-BEAE-2007d0668476" ab und leitet Sie an das Get-AzADAppCredential-Cmdlet weiter, um alle Anmeldeinformationen für diese Anwendung aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="7b93b-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="7b93b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b93b-117">PARAMETERS</span></span>

### <span data-ttu-id="7b93b-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7b93b-118">-ApplicationId</span></span>
<span data-ttu-id="7b93b-119">Die ID der Anwendung, aus der Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7b93b-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="7b93b-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="7b93b-120">-ApplicationObject</span></span>
<span data-ttu-id="7b93b-121">Das Application-Objekt, aus dem Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7b93b-121">The application object to retrieve credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b93b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b93b-122">-DefaultProfile</span></span>
<span data-ttu-id="7b93b-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7b93b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b93b-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7b93b-124">-DisplayName</span></span>
<span data-ttu-id="7b93b-125">Der Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7b93b-125">The display name of the application.</span></span>

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

### <span data-ttu-id="7b93b-126">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="7b93b-126">-ObjectId</span></span>
<span data-ttu-id="7b93b-127">Die Objekt-ID der Anwendung, aus der Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7b93b-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="7b93b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b93b-128">CommonParameters</span></span>
<span data-ttu-id="7b93b-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b93b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b93b-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b93b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b93b-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b93b-131">INPUTS</span></span>

### <span data-ttu-id="7b93b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7b93b-132">System.String</span></span>

### <span data-ttu-id="7b93b-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="7b93b-133">System.Guid</span></span>

### <span data-ttu-id="7b93b-134">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="7b93b-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="7b93b-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b93b-135">OUTPUTS</span></span>

### <span data-ttu-id="7b93b-136">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="7b93b-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="7b93b-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b93b-137">NOTES</span></span>

## <span data-ttu-id="7b93b-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b93b-138">RELATED LINKS</span></span>

[<span data-ttu-id="7b93b-139">Neu – AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7b93b-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="7b93b-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7b93b-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="7b93b-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="7b93b-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

