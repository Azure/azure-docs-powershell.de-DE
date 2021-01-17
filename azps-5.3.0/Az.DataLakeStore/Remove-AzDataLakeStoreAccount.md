---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
ms.openlocfilehash: 75af40b104bbf6ffa65211087572140a070b71e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458063"
---
# <span data-ttu-id="d2ed9-101">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d2ed9-101">Remove-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="d2ed9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2ed9-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ed9-103">Löscht ein Data Lake Store-Konto endgültig.</span><span class="sxs-lookup"><span data-stu-id="d2ed9-103">Deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="d2ed9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2ed9-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2ed9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2ed9-105">DESCRIPTION</span></span>
<span data-ttu-id="d2ed9-106">Das **Cmdlet "Remove-AzDataLakeStoreAccount"** löscht ein Data Lake Store-Konto dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="d2ed9-106">The **Remove-AzDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="d2ed9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d2ed9-107">EXAMPLES</span></span>

### <span data-ttu-id="d2ed9-108">Beispiel 1: Entfernen eines Data Lake Store-Kontos</span><span class="sxs-lookup"><span data-stu-id="d2ed9-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="d2ed9-109">Mit diesem Befehl wird das Konto "ContosoADL" aus dem Data Lake Store entfernt.</span><span class="sxs-lookup"><span data-stu-id="d2ed9-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="d2ed9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2ed9-110">PARAMETERS</span></span>

### <span data-ttu-id="d2ed9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ed9-111">-DefaultProfile</span></span>
<span data-ttu-id="d2ed9-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d2ed9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2ed9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d2ed9-113">-Force</span></span>
<span data-ttu-id="d2ed9-114">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="d2ed9-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ed9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d2ed9-115">-Name</span></span>
<span data-ttu-id="d2ed9-116">Gibt den Namen des zu entfernenden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="d2ed9-116">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="d2ed9-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2ed9-117">-PassThru</span></span>
<span data-ttu-id="d2ed9-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d2ed9-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d2ed9-119">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="d2ed9-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2ed9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ed9-120">-ResourceGroupName</span></span>
<span data-ttu-id="d2ed9-121">Gibt die Ressourcengruppe an, die das zu entfernende Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="d2ed9-121">Specifies the resource group that contains the account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2ed9-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2ed9-122">-Confirm</span></span>
<span data-ttu-id="d2ed9-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2ed9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2ed9-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d2ed9-124">-WhatIf</span></span>
<span data-ttu-id="d2ed9-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2ed9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2ed9-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2ed9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2ed9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ed9-127">CommonParameters</span></span>
<span data-ttu-id="d2ed9-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2ed9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ed9-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2ed9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ed9-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d2ed9-130">INPUTS</span></span>

### <span data-ttu-id="d2ed9-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d2ed9-131">System.String</span></span>

## <span data-ttu-id="d2ed9-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d2ed9-132">OUTPUTS</span></span>

### <span data-ttu-id="d2ed9-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d2ed9-133">System.Boolean</span></span>

## <span data-ttu-id="d2ed9-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d2ed9-134">NOTES</span></span>

## <span data-ttu-id="d2ed9-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d2ed9-135">RELATED LINKS</span></span>

[<span data-ttu-id="d2ed9-136">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d2ed9-136">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="d2ed9-137">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d2ed9-137">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="d2ed9-138">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d2ed9-138">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="d2ed9-139">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d2ed9-139">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


