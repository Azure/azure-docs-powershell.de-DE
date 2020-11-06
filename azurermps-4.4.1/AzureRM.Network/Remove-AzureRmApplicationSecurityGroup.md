---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: b0387d10950073c4655c6e6015edc6957ae14edc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497066"
---
# <span data-ttu-id="2df6c-101">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2df6c-101">Remove-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="2df6c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2df6c-102">SYNOPSIS</span></span>
<span data-ttu-id="2df6c-103">Entfernt eine Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2df6c-103">Removes an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2df6c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2df6c-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2df6c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2df6c-105">DESCRIPTION</span></span>
<span data-ttu-id="2df6c-106">Das Cmdlet " **Remove-AzureRmApplicationSecurityGroup** " entfernt eine Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2df6c-106">The **Remove-AzureRmApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="2df6c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2df6c-107">EXAMPLES</span></span>

### <span data-ttu-id="2df6c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2df6c-108">Example 1</span></span>
```
PS C:\>Remove-AzureRmApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="2df6c-109">Mit diesem Befehl wird eine Anwendungs Sicherheitsgruppe namens "MyApplicationSecurityGrouo" in der Ressourcengruppe "myresourcegroup" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2df6c-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="2df6c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2df6c-110">PARAMETERS</span></span>

### <span data-ttu-id="2df6c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df6c-111">-DefaultProfile</span></span>
<span data-ttu-id="2df6c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2df6c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2df6c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2df6c-113">-Force</span></span>
<span data-ttu-id="2df6c-114">Keine Bestätigung anfordern, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="2df6c-114">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="2df6c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2df6c-115">-Name</span></span>
<span data-ttu-id="2df6c-116">Der Name der Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2df6c-116">The name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df6c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2df6c-117">-PassThru</span></span>
<span data-ttu-id="2df6c-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2df6c-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="2df6c-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="2df6c-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2df6c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2df6c-120">-ResourceGroupName</span></span>
<span data-ttu-id="2df6c-121">Der Ressourcengruppenname der Anwendungs Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="2df6c-121">The resource group name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df6c-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2df6c-122">-Confirm</span></span>
<span data-ttu-id="2df6c-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2df6c-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df6c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2df6c-124">-WhatIf</span></span>
<span data-ttu-id="2df6c-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2df6c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2df6c-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2df6c-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df6c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df6c-127">CommonParameters</span></span>
<span data-ttu-id="2df6c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2df6c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df6c-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2df6c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df6c-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2df6c-130">INPUTS</span></span>

### <span data-ttu-id="2df6c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2df6c-131">System.String</span></span>

## <span data-ttu-id="2df6c-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2df6c-132">OUTPUTS</span></span>

### <span data-ttu-id="2df6c-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="2df6c-133">System.Object</span></span>

## <span data-ttu-id="2df6c-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="2df6c-134">NOTES</span></span>

## <span data-ttu-id="2df6c-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2df6c-135">RELATED LINKS</span></span>

[<span data-ttu-id="2df6c-136">Neu – AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2df6c-136">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="2df6c-137">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2df6c-137">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)
