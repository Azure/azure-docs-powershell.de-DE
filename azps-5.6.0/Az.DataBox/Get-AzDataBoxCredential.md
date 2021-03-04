---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: f5f811b28b349c6dbc9972c9a464a56a002b99f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942987"
---
# <span data-ttu-id="d5ff6-101">Get-AzDataBoxCredential</span><span class="sxs-lookup"><span data-stu-id="d5ff6-101">Get-AzDataBoxCredential</span></span>

## <span data-ttu-id="d5ff6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5ff6-102">SYNOPSIS</span></span>
<span data-ttu-id="d5ff6-103">Ruft die Datenboxanmeldeinformationen eines bestimmten Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="d5ff6-103">Gets the databox credentials of a specific job</span></span>

## <span data-ttu-id="d5ff6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5ff6-104">SYNTAX</span></span>

### <span data-ttu-id="d5ff6-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5ff6-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5ff6-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5ff6-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5ff6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5ff6-107">DESCRIPTION</span></span>
<span data-ttu-id="d5ff6-108">Das **Get-AzDataBoxCredential-Cmdlet** ruft die Anmeldeinformationen des Datenfelds eines bestimmten Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="d5ff6-108">The **Get-AzDataBoxCredential** cmdlet gets the credentials of the databox of a specific job.</span></span> <span data-ttu-id="d5ff6-109">Die internen Eigenschaften des zurückgegebenen Anmeldeinformationsobjekts unterscheiden sich für unterschiedliche Sku-Typen.</span><span class="sxs-lookup"><span data-stu-id="d5ff6-109">The internal properties of the returned credentials object will be different for different Sku types.</span></span>

## <span data-ttu-id="d5ff6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d5ff6-110">EXAMPLES</span></span>

### <span data-ttu-id="d5ff6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d5ff6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="d5ff6-112">Dadurch werden die JobSecrets des angegebenen Auftrags neu festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d5ff6-112">This retuns the JobSecrets of the specified job</span></span>

### <span data-ttu-id="d5ff6-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d5ff6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="d5ff6-114">Dadurch werden die JobSecrets des angegebenen Auftrags neu festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d5ff6-114">This retuns the JobSecrets of the specified job</span></span>

## <span data-ttu-id="d5ff6-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d5ff6-115">PARAMETERS</span></span>

### <span data-ttu-id="d5ff6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ff6-116">-DefaultProfile</span></span>
<span data-ttu-id="d5ff6-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5ff6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5ff6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d5ff6-118">-Name</span></span>
<span data-ttu-id="d5ff6-119">Name des Databox-Auftrags</span><span class="sxs-lookup"><span data-stu-id="d5ff6-119">Databox Job Name</span></span>

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

### <span data-ttu-id="d5ff6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5ff6-120">-ResourceGroupName</span></span>
<span data-ttu-id="d5ff6-121">Name der Databox-Jobressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d5ff6-121">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="d5ff6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5ff6-122">-ResourceId</span></span>
<span data-ttu-id="d5ff6-123">Databox Job Resource Id</span><span class="sxs-lookup"><span data-stu-id="d5ff6-123">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="d5ff6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5ff6-124">CommonParameters</span></span>
<span data-ttu-id="d5ff6-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5ff6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5ff6-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5ff6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5ff6-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d5ff6-127">INPUTS</span></span>

### <span data-ttu-id="d5ff6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d5ff6-128">System.String</span></span>

## <span data-ttu-id="d5ff6-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d5ff6-129">OUTPUTS</span></span>

### <span data-ttu-id="d5ff6-130">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="d5ff6-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="d5ff6-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d5ff6-131">NOTES</span></span>

## <span data-ttu-id="d5ff6-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d5ff6-132">RELATED LINKS</span></span>
