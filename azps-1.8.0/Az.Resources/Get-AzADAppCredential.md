---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: fdef07255316b1d7529202c36b844e8732c76390
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659670"
---
# <span data-ttu-id="e4fcc-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e4fcc-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="e4fcc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e4fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="e4fcc-103">Ruft eine Liste der Anmeldeinformationen ab, die einer Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e4fcc-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="e4fcc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4fcc-104">SYNTAX</span></span>

### <span data-ttu-id="e4fcc-105">ApplicationObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e4fcc-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4fcc-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4fcc-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4fcc-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4fcc-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4fcc-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4fcc-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4fcc-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e4fcc-109">DESCRIPTION</span></span>
<span data-ttu-id="e4fcc-110">Das Get-AzADAppCredential-Cmdlet kann verwendet werden, um eine Liste der Anmeldeinformationen abzurufen, die einer Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e4fcc-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="e4fcc-111">Dieser Befehl ruft alle Anmelde Informationseigenschaften (aber nicht den Wert der Anmeldeinformationen) ab, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e4fcc-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="e4fcc-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e4fcc-112">EXAMPLES</span></span>

### <span data-ttu-id="e4fcc-113">Beispiel 1: Abrufen von Anwendungs Anmeldeinformationen nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="e4fcc-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="e4fcc-114">Gibt eine Liste der Anmeldeinformationen zurück, die der Anwendung zugeordnet sind, die die Objekt-ID "1f99cf81-0146-4f4e-BEAE-2007d0668476" hat.</span><span class="sxs-lookup"><span data-stu-id="e4fcc-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="e4fcc-115">Beispiel 2 – Abrufen von Anwendungs Anmeldeinformationen durch Piping</span><span class="sxs-lookup"><span data-stu-id="e4fcc-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="e4fcc-116">Ruft die Anwendung mit der Objekt-ID "1f99cf81-0146-4f4e-BEAE-2007d0668476" ab und leitet Sie an das Get-AzADAppCredential-Cmdlet weiter, um alle Anmeldeinformationen für diese Anwendung aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="e4fcc-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="e4fcc-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4fcc-117">PARAMETERS</span></span>

### <span data-ttu-id="e4fcc-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e4fcc-118">-ApplicationId</span></span>
<span data-ttu-id="e4fcc-119">Die ID der Anwendung, aus der Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e4fcc-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="e4fcc-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="e4fcc-120">-ApplicationObject</span></span>
<span data-ttu-id="e4fcc-121">Das Application-Objekt, aus dem Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e4fcc-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="e4fcc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4fcc-122">-DefaultProfile</span></span>
<span data-ttu-id="e4fcc-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e4fcc-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4fcc-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e4fcc-124">-DisplayName</span></span>
<span data-ttu-id="e4fcc-125">Der Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e4fcc-125">The display name of the application.</span></span>

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

### <span data-ttu-id="e4fcc-126">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="e4fcc-126">-ObjectId</span></span>
<span data-ttu-id="e4fcc-127">Die Objekt-ID der Anwendung, aus der Anmeldeinformationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e4fcc-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="e4fcc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4fcc-128">CommonParameters</span></span>
<span data-ttu-id="e4fcc-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4fcc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4fcc-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4fcc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4fcc-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e4fcc-131">INPUTS</span></span>

### <span data-ttu-id="e4fcc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e4fcc-132">System.String</span></span>

### <span data-ttu-id="e4fcc-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e4fcc-133">System.Guid</span></span>

### <span data-ttu-id="e4fcc-134">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="e4fcc-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="e4fcc-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e4fcc-135">OUTPUTS</span></span>

### <span data-ttu-id="e4fcc-136">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="e4fcc-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="e4fcc-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="e4fcc-137">NOTES</span></span>

## <span data-ttu-id="e4fcc-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e4fcc-138">RELATED LINKS</span></span>

[<span data-ttu-id="e4fcc-139">Neu – AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e4fcc-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="e4fcc-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e4fcc-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="e4fcc-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e4fcc-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

