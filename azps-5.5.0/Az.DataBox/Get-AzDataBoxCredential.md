---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: 308f7aa185350635815622ed684e47ebea349f9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148369"
---
# <span data-ttu-id="474ae-101">Get-AzDataBoxCredential</span><span class="sxs-lookup"><span data-stu-id="474ae-101">Get-AzDataBoxCredential</span></span>

## <span data-ttu-id="474ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="474ae-102">SYNOPSIS</span></span>
<span data-ttu-id="474ae-103">Ruft die Anmeldeinformationen für das Datenfeld eines bestimmten Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="474ae-103">Gets the databox credentials of a specific job</span></span>

## <span data-ttu-id="474ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="474ae-104">SYNTAX</span></span>

### <span data-ttu-id="474ae-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="474ae-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="474ae-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="474ae-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="474ae-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="474ae-107">DESCRIPTION</span></span>
<span data-ttu-id="474ae-108">Das **Cmdlet "Get-AzDataBoxCredential"** ruft die Anmeldeinformationen des Datenfelds eines bestimmten Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="474ae-108">The **Get-AzDataBoxCredential** cmdlet gets the credentials of the databox of a specific job.</span></span> <span data-ttu-id="474ae-109">Die internen Eigenschaften des zurückgegebenen Anmeldeinformationsobjekts unterscheiden sich für unterschiedliche SKU-Typen.</span><span class="sxs-lookup"><span data-stu-id="474ae-109">The internal properties of the returned credentials object will be different for different Sku types.</span></span>

## <span data-ttu-id="474ae-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="474ae-110">EXAMPLES</span></span>

### <span data-ttu-id="474ae-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="474ae-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="474ae-112">Dadurch werden die JobSecrets des angegebenen Auftrags neu festgelegt</span><span class="sxs-lookup"><span data-stu-id="474ae-112">This retuns the JobSecrets of the specified job</span></span>

### <span data-ttu-id="474ae-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="474ae-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="474ae-114">Dadurch werden die JobSecrets des angegebenen Auftrags neu festgelegt</span><span class="sxs-lookup"><span data-stu-id="474ae-114">This retuns the JobSecrets of the specified job</span></span>

## <span data-ttu-id="474ae-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="474ae-115">PARAMETERS</span></span>

### <span data-ttu-id="474ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="474ae-116">-DefaultProfile</span></span>
<span data-ttu-id="474ae-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="474ae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="474ae-118">-Name</span><span class="sxs-lookup"><span data-stu-id="474ae-118">-Name</span></span>
<span data-ttu-id="474ae-119">Name des Datenfeldauftrags</span><span class="sxs-lookup"><span data-stu-id="474ae-119">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="474ae-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="474ae-120">-ResourceGroupName</span></span>
<span data-ttu-id="474ae-121">Name der Databox-Auftragsressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="474ae-121">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="474ae-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="474ae-122">-ResourceId</span></span>
<span data-ttu-id="474ae-123">Databox Job Resource Id</span><span class="sxs-lookup"><span data-stu-id="474ae-123">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="474ae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="474ae-124">CommonParameters</span></span>
<span data-ttu-id="474ae-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="474ae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="474ae-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="474ae-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="474ae-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="474ae-127">INPUTS</span></span>

### <span data-ttu-id="474ae-128">System.String</span><span class="sxs-lookup"><span data-stu-id="474ae-128">System.String</span></span>

## <span data-ttu-id="474ae-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="474ae-129">OUTPUTS</span></span>

### <span data-ttu-id="474ae-130">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="474ae-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="474ae-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="474ae-131">NOTES</span></span>

## <span data-ttu-id="474ae-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="474ae-132">RELATED LINKS</span></span>
