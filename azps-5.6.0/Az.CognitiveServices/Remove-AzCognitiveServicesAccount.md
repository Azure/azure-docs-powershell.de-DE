---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: f35aee632f4f5c5ee2be36ac3eea92c5ec5f59f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939656"
---
# <span data-ttu-id="10053-101">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="10053-101">Remove-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="10053-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10053-102">SYNOPSIS</span></span>
<span data-ttu-id="10053-103">Löscht ein Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="10053-103">Deletes a Cognitive Services account.</span></span>

## <span data-ttu-id="10053-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10053-104">SYNTAX</span></span>

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10053-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10053-105">DESCRIPTION</span></span>
<span data-ttu-id="10053-106">Das **Cmdlet Remove-AzCognitiveServicesAccount** löscht das angegebene Cognitive Services-Konto.</span><span class="sxs-lookup"><span data-stu-id="10053-106">The **Remove-AzCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="10053-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="10053-107">EXAMPLES</span></span>

### <span data-ttu-id="10053-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="10053-108">Example 1</span></span>
<span data-ttu-id="10053-109">Dieser Befehl gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="10053-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="10053-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="10053-110">PARAMETERS</span></span>

### <span data-ttu-id="10053-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10053-111">-DefaultProfile</span></span>
<span data-ttu-id="10053-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="10053-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10053-113">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="10053-113">-Force</span></span>
<span data-ttu-id="10053-114">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="10053-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10053-115">-Name</span><span class="sxs-lookup"><span data-stu-id="10053-115">-Name</span></span>
<span data-ttu-id="10053-116">Gibt den Namen des zu löschenden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="10053-116">Specifies the name of the account to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10053-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10053-117">-ResourceGroupName</span></span>
<span data-ttu-id="10053-118">Gibt den Namen der Ressourcengruppe an, der das Cognitive Services-Konto zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="10053-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10053-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="10053-119">-Confirm</span></span>
<span data-ttu-id="10053-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="10053-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10053-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10053-121">-WhatIf</span></span>
<span data-ttu-id="10053-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="10053-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10053-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="10053-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10053-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10053-124">CommonParameters</span></span>
<span data-ttu-id="10053-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10053-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10053-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10053-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10053-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="10053-127">INPUTS</span></span>

### <span data-ttu-id="10053-128">System.String</span><span class="sxs-lookup"><span data-stu-id="10053-128">System.String</span></span>

## <span data-ttu-id="10053-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="10053-129">OUTPUTS</span></span>

### <span data-ttu-id="10053-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="10053-130">System.Void</span></span>

## <span data-ttu-id="10053-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="10053-131">NOTES</span></span>

## <span data-ttu-id="10053-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="10053-132">RELATED LINKS</span></span>

[<span data-ttu-id="10053-133">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="10053-133">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="10053-134">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="10053-134">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="10053-135">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="10053-135">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


