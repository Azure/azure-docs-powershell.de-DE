---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: 7bfa908e83d7731ca2ed5613d82f42b19c392b2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146145"
---
# <span data-ttu-id="e1e06-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e1e06-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="e1e06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1e06-102">SYNOPSIS</span></span>
<span data-ttu-id="e1e06-103">Ruft eine Liste der Anmeldeinformationen ab, die einer Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e1e06-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="e1e06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1e06-104">SYNTAX</span></span>

### <span data-ttu-id="e1e06-105">ApplicationObjectIdParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e1e06-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1e06-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1e06-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1e06-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1e06-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1e06-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1e06-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1e06-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1e06-109">DESCRIPTION</span></span>
<span data-ttu-id="e1e06-110">Das Get-AzADAppCredential cmdlet kann verwendet werden, um eine Liste der Anmeldeinformationen abzurufen, die einer Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e1e06-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="e1e06-111">Mit diesem Befehl werden alle Anmeldeinformationseigenschaften (aber nicht der Wert für die Anmeldeinformationen) abgerufen, die der Anwendung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e1e06-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="e1e06-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e1e06-112">EXAMPLES</span></span>

### <span data-ttu-id="e1e06-113">Beispiel 1: Erhalten von Anwendungsanmeldeinformationen nach Objekt-ID</span><span class="sxs-lookup"><span data-stu-id="e1e06-113">Example 1: Get application credentials by object id</span></span>

```powershell
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="e1e06-114">Gibt eine Liste der Anmeldeinformationen zurück, die der Anwendung mit der Objekt-ID '1f99cf81-0146-4f4e-beae-2007d0668476' zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e1e06-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="e1e06-115">Beispiel 2: Erhalten von Anwendungsanmeldeinformationen durch Piping</span><span class="sxs-lookup"><span data-stu-id="e1e06-115">Example 2: Get application credentials by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="e1e06-116">Ruft die Anwendung mit der Objekt-ID '1f99cf81-0146-4f4e-beae-2007d0668476' ab und gibt sie an das Cmdlet Get-AzADAppCredential weiter, um alle Anmeldeinformationen für diese Anwendung auflisten.</span><span class="sxs-lookup"><span data-stu-id="e1e06-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="e1e06-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1e06-117">PARAMETERS</span></span>

### <span data-ttu-id="e1e06-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e1e06-118">-ApplicationId</span></span>
<span data-ttu-id="e1e06-119">Die ID der Anwendung, aus der Anmeldeinformationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e1e06-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="e1e06-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="e1e06-120">-ApplicationObject</span></span>
<span data-ttu-id="e1e06-121">Das Anwendungsobjekt, aus dem Anmeldeinformationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e1e06-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="e1e06-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1e06-122">-DefaultProfile</span></span>
<span data-ttu-id="e1e06-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e1e06-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1e06-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e1e06-124">-DisplayName</span></span>
<span data-ttu-id="e1e06-125">Der Anzeigename der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e1e06-125">The display name of the application.</span></span>

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

### <span data-ttu-id="e1e06-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e1e06-126">-ObjectId</span></span>
<span data-ttu-id="e1e06-127">Die Objekt-ID der Anwendung, aus der Anmeldeinformationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e1e06-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="e1e06-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1e06-128">CommonParameters</span></span>
<span data-ttu-id="e1e06-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1e06-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1e06-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1e06-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1e06-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e1e06-131">INPUTS</span></span>

### <span data-ttu-id="e1e06-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e1e06-132">System.String</span></span>

### <span data-ttu-id="e1e06-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e1e06-133">System.Guid</span></span>

### <span data-ttu-id="e1e06-134">Microsoft.Azure.Commands.ActiveDirectory.WERDENDApplication</span><span class="sxs-lookup"><span data-stu-id="e1e06-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="e1e06-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e1e06-135">OUTPUTS</span></span>

### <span data-ttu-id="e1e06-136">Microsoft.Azure.Commands.ActiveDirectory.ODERDCredential</span><span class="sxs-lookup"><span data-stu-id="e1e06-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="e1e06-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e1e06-137">NOTES</span></span>

## <span data-ttu-id="e1e06-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e1e06-138">RELATED LINKS</span></span>

[<span data-ttu-id="e1e06-139">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e1e06-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="e1e06-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e1e06-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="e1e06-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e1e06-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

